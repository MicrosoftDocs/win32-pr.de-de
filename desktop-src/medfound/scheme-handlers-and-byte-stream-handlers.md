---
description: In diesem Thema werden die internen Details zur Erstellung einer Medienquelle durch den Quellre resolver beschrieben.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Schemahandler und Byte-Stream Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7bde81a02762cd9c82e0a7d031582c856da6984ab231775580ddf249caca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058229"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Schemahandler und Byte-Stream Handler

In diesem Thema werden die internen Details zur Erstellung einer Medienquelle durch den Quellre resolver beschrieben. Lesen Sie dieses Thema, wenn Sie eine benutzerdefinierte Medienquelle für Media Foundation implementieren und möchten, dass die Medienquelle für Anwendungen über den Quell resolver verfügbar ist.

Der Quelllöser kann eine Medienquelle aus einer URL oder aus einem Bytestream (d. b. einem [**POINTERByteStream-Zeiger)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) erstellen. Dazu werden Hilfsobjekte verwendet, die als Handler bezeichnet *werden.* Für URLs verwendet der Quell resolver *Schemahandler.* Für Bytestreams werden *Bytestreamhandler verwendet.*

Ein Schemahandler verwendet eine URL als Eingabe und erstellt entweder eine Medienquelle oder einen Bytestream. Wenn ein Bytestream erstellt wird, übergibt der Quell resolver diesen an einen Bytestreamhandler, der die Medienquelle erstellt. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm des Quellauflösungsprozesses](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Schemahandler

Schemahandler werden verwendet, wenn die Anwendung [**DEN SOURCESourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) oder die asynchrone Entsprechung [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)aufruft.

Der Quell resolver sucht schema handlers in der Registrierung. Schemahandler werden nach URL-Schema unter den folgenden Schlüsseln aufgelistet:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

dabei *<scheme>* ist das URL-Schema, das der Handler analysieren soll. Das Schema enthält das nachfolgende Zeichen ":". Beispiel: "http:".

Um einen neuen Schemahandler zu registrieren, fügen Sie einen Eintrag hinzu, dessen Name die CLSID des Schemahandlers ist, in kanonischer Zeichenfolgenform: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Der Wert des Eintrags ist eine Zeichenfolge (REG \_ SZ), die eine kurze Beschreibung des Handlers enthält, z. B. "Mein Schemahandler". Der wichtige Teil des Eintrags ist die CLSID. Der Quellre resolver erstellt den Handler durch Aufrufen von **CoCreateInstance** mit dieser CLSID.

Schemahandler machen die [**INTERFACESSchemeHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) verfügbar. Wenn der Quellre resolver einen Schemahandler findet, der dem URL-Schema entspricht, ruft der Quellre resolver [**DENSCHEMEHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)auf und übergibt die ursprüngliche URL. Der Schemahandler öffnet die URL und versucht, den Inhalt zu analysieren. An diesem Punkt verfügt der Schemahandler über zwei Optionen:

-   Erstellen Sie eine Medienquelle.
-   Erstellen Sie einen Bytestream.

Wenn eine Medienquelle erstellt wird, gibt der Quell resolver die Medienquelle an die Anwendung zurück. Wenn ein Bytestream erstellt wird, versucht der Quell resolver, einen geeigneten Bytestreamhandler zu finden, wie im nächsten Abschnitt beschrieben.

## <a name="byte-stream-handlers"></a>Byte-Stream Handler

Bytestreamhandler werden verwendet, wenn die Anwendung [**DEN HANDLERSOURCEResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) oder die asynchrone Entsprechung [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)aufruft. Sie werden auch verwendet, wenn ein Schemahandler einen Bytestream zurückgibt, wie zuvor beschrieben.

Wie bei Schemahandlern werden byte-stream-Handler in der Registrierung aufgeführt. Sie werden entweder nach Dateinamenerweiterung oder MIME-Typ (oder beidem) unter den folgenden Schlüsseln aufgeführt:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

dabei *<ExtensionOrMimeType>* ist die Dateinamenerweiterung oder der MIME-Typ. Dateierweiterungen enthalten das anfängliche Zeichen ".". Beispiel: ".wmv".

Die Dateinamenerweiterung ist Teil der URL, die von der Anwendung bereitgestellt wird. Der MIME-Typ kann über das [**MF \_ BYTESTREAM \_ CONTENT \_ TYPE-Attribut**](mf-bytestream-content-type-attribute.md) im Bytestream verfügbar sein.

Um einen neuen Bytestreamhandler zu registrieren, fügen Sie einen Eintrag hinzu, dessen Name die CLSID des Handlers ist, in kanonischer Zeichenfolgenform. Der Wert des Eintrags ist eine Zeichenfolge (REG \_ SZ), die eine kurze Beschreibung des Handlers enthält, z. B. "My Byte-Stream Handler". Der Quellre resolver ruft **CoCreateInstance** auf, um den Handler aus der CLSID zu erstellen. Sie können denselben Handler unter mehreren Erweiterungen oder MIME-Typen registrieren.

Bytestreamhandler machen die [**INTERFACESByteStreamHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) verfügbar. Wenn der Quellre resolver einen übereinstimmenden Bytestreamhandler findet, ruft er [**DENBYTEStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)auf. Die Eingabe für diese Methode ist ein Zeiger auf den Bytestream sowie ggf. die ursprüngliche URL. Der Bytestreamhandler liest aus dem Bytestream, bis er genügend Daten analysiert, um die Medienquelle zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quelllöser](source-resolver.md)
</dt> </dl>

 

 



