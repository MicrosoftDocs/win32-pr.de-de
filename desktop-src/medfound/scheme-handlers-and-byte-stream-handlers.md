---
description: In diesem Thema werden die internen Details dazu beschrieben, wie der Quellre resolver eine Medienquelle erstellt.
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

In diesem Thema werden die internen Details dazu beschrieben, wie der Quellre resolver eine Medienquelle erstellt. Lesen Sie dieses Thema, wenn Sie eine benutzerdefinierte Medienquelle für Media Foundation implementieren und die Medienquelle für Anwendungen über den Quellre resolver verfügbar sein soll.

Der Quellre konfliktlöser kann eine Medienquelle aus einer URL oder aus einem Bytestream (d. h. einem [**DURCHBYTEStream-Zeiger)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) erstellen. Zu diesem Zwecke werden Hilfsobjekte verwendet, die *handlers genannt werden.* Für URLs verwendet der Quellre resolver *die Schemahandler*. Für Bytestreams werden *Bytestreamhandler verwendet.*

Ein Schemahandler verwendet eine URL als Eingabe und erstellt entweder eine Medienquelle oder einen Bytestream. Wenn ein Bytestream erstellt wird, über gibt der Quellre resolver diesen an einen Bytestreamhandler weiter, der die Medienquelle erstellt. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das den Quellauflösungsprozess zeigt](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Schemahandler

Schemahandler werden verwendet, wenn die Anwendung [**DEN TYPSOURCEResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) oder die asynchrone Entsprechung [**BeginCreateObjectFromURL aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)

Der Quellre resolver sucht Schemahandler in der Registrierung. Schemahandler werden nach URL-Schema unter den folgenden Schlüsseln aufgelistet:

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

dabei *<scheme>* ist das URL-Schema, das der Handler analysieren soll. Das Schema enthält das folgende Zeichen ":". Beispiel: "http:".

Um einen neuen Schemahandler zu registrieren, fügen Sie einen Eintrag hinzu, dessen Name die CLSID des Schemahandlers in kanonischer Zeichenfolgenform ist: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Der Wert des Eintrags ist eine Zeichenfolge (REG SZ), die eine kurze Beschreibung des Handlers enthält, z. \_ B. "Mein Schemahandler". Der wichtige Teil des Eintrags ist die CLSID. Der Quellre resolver erstellt den Handler, indem er **CoCreateInstance mit** dieser CLSID aufruft.

Schemahandler machen die [**BENUTZEROBERFLÄCHESchemeHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) verfügbar. Wenn der Quellre resolver einen Schemahandler findet, der dem URL-Schema entspricht, ruft der Quellre konfliktlöser [**DENKSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)auf und über gibt die ursprüngliche URL an. Der Schemahandler öffnet die URL und versucht, den Inhalt zu analysieren. An diesem Punkt verfügt der Schemahandler über zwei Optionen:

-   Erstellen Sie eine Medienquelle.
-   Erstellen Sie einen Bytestream.

Wenn eine Medienquelle erstellt wird, gibt der Quellre resolver die Medienquelle an die Anwendung zurück. Wenn ein Bytestream erstellt wird, versucht der Quellre resolver, einen geeigneten Bytestreamhandler zu finden, wie im nächsten Abschnitt beschrieben.

## <a name="byte-stream-handlers"></a>Byte-Stream Handler

Bytestream-Handler werden verwendet, wenn die Anwendung [**DEN TYPSOURCEResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) oder die asynchrone Entsprechung [**BeginCreateObjectFromByteStream aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) Sie werden auch verwendet, wenn ein Schemahandler wie zuvor beschrieben einen Bytestream zurückgibt.

Wie bei Schemahandlern werden bytestream-Handler in der Registrierung aufgeführt. Sie werden entweder nach Dateierweiterung oder MIME-Typ (oder beidem) unter den folgenden Schlüsseln aufgeführt:

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

dabei *<ExtensionOrMimeType>* ist die Dateierweiterung oder der MIME-Typ. Dateierweiterungen enthalten das anfangs "."-Zeichen. Beispiel: ".wmv".

Die Dateinamenerweiterung ist Teil der URL, die von der Anwendung bereitgestellt wird. Der MIME-Typ ist möglicherweise über das [**MF \_ BYTESTREAM \_ CONTENT \_ TYPE-Attribut**](mf-bytestream-content-type-attribute.md) im Bytestream verfügbar.

Um einen neuen Bytestreamhandler zu registrieren, fügen Sie einen Eintrag hinzu, dessen Name die CLSID des Handlers in kanonischer Zeichenfolgenform ist. Der Wert des Eintrags ist eine Zeichenfolge (REG SZ), die eine kurze Beschreibung des Handlers enthält, z. B. \_ "My Byte-Stream Handler". Der Quellre resolver ruft **CoCreateInstance auf,** um den Handler aus der CLSID zu erstellen. Sie können denselben Handler unter mehr als einer Erweiterung oder einem MIME-Typ registrieren.

Bytestreamhandler machen die [**BESBYTEStreamHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) verfügbar. Wenn der Quellre resolver einen übereinstimmenden Bytestreamhandler findet, ruft er [**DEN TYPBYTEStreamHandler::BeginCreateObject auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) Die Eingabe für diese Methode ist ein Zeiger auf den Bytestream sowie die ursprüngliche URL( falls verfügbar). Der Bytestreamhandler liest aus dem Bytestream, bis er genügend Daten analysiert, um die Medienquelle zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellre resolver](source-resolver.md)
</dt> </dl>

 

 



