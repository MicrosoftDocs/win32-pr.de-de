---
description: In diesem Thema werden die internen Details erläutert, wie der quellresolver eine Medienquelle erstellt.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Schema Handler und Byte-Stream Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359934"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Schema Handler und Byte-Stream Handler

In diesem Thema werden die internen Details erläutert, wie der quellresolver eine Medienquelle erstellt. Lesen Sie dieses Thema, wenn Sie eine benutzerdefinierte Medienquelle für Media Foundation implementieren und die Medienquelle für Anwendungen über den quellresolver verfügbar sein soll.

Der quellresolver kann eine Medienquelle aus einer URL oder einem Bytestream erstellen (d. h. ein [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Zeiger). Hierfür werden Hilfsobjekte verwendet, die als *Handler* bezeichnet werden. Für URLs verwendet der quellresolver *Schema Handler*. Für Bytestreams werden *Byte Datenstrom Handler* verwendet.

Ein Schema Handler nimmt eine URL als Eingabe an und erstellt entweder eine Medienquelle oder einen Bytestream. Wenn ein Bytestream erstellt wird, übergibt der quellresolver diesen an einen bytestreamhandler, der die Medienquelle erstellt. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Diagramm, das den Quell Auflösungsprozess anzeigt](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Schema Handler

Schema Handler werden verwendet, wenn die Anwendung [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) oder die zugehörige asynchrone Entsprechung [**beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)aufruft.

Der Quell Konflikt Löser sucht Schema Handler in der Registrierung. Schema Handler werden nach dem URL-Schema unter den folgenden Schlüsseln aufgelistet:

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

dabei *<scheme>* ist das URL-Schema, das der Handler analysieren soll. Das Schema enthält das nachfolgende Zeichen ': '; Beispiel: "http:".

Fügen Sie zum Registrieren eines neuen Schema Handlers einen Eintrag hinzu, dessen Name die CLSID des Schema Handlers ist, in kanonischer Zeichen folgen Form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Der Wert des Eintrags ist eine Zeichenfolge (reg \_ SZ), die eine kurze Beschreibung des Handlers enthält, z. b. "Mein Schema Handler". Der wichtige Teil des Eintrags ist die CLSID. Der quellresolver erstellt den Handler durch Aufrufen von **CoCreateInstance** mit dieser CLSID.

Schema Handler machen die [**IMF Schema Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) -Schnittstelle verfügbar. Wenn der quellresolver einen Schema Handler findet, der mit dem URL-Schema übereinstimmt, ruft der quellresolver [**imvschemehandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)auf und übergibt dabei die ursprüngliche URL. Der Schema Handler öffnet die URL und versucht, den Inhalt zu analysieren. An diesem Punkt verfügt der Schema Handler über zwei Optionen:

-   Erstellen Sie eine Medienquelle.
-   Erstellen Sie einen Bytestream.

Wenn eine Medienquelle erstellt wird, gibt der quellresolver die Medienquelle an die Anwendung zurück. Wenn ein Bytestream erstellt wird, versucht der quellresolver, einen entsprechenden bytestreamhandler zu finden, wie im nächsten Abschnitt beschrieben.

## <a name="byte-stream-handlers"></a>Byte-Stream Handler

Byte-Datenstrom Handler werden verwendet, wenn die Anwendung [**IMF sourceresolver:: forateobjectfrooltestream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) oder die zugehörige asynchrone Entsprechung ( [**beginkreateobjectfromb-Stream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)) aufruft. Sie werden auch verwendet, wenn ein Schema Handler einen Bytestream zurückgibt, wie zuvor beschrieben.

Wie bei Schema Handlern sind Byte-Stream-Handler in der Registrierung aufgeführt. Sie werden entweder über die Dateinamenerweiterung oder den MIME-Typ (oder beides) unter den folgenden Schlüsseln aufgelistet:

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

dabei *<ExtensionOrMimeType>* ist die Dateinamenerweiterung oder der MIME-Typ. Dateierweiterungen enthalten das erste Zeichen ".". Beispiel: ". wmv".

Die Dateinamenerweiterung ist Teil der URL, die von der Anwendung bereitgestellt wird. Der MIME-Typ ist möglicherweise über das [**MF- \_ Bytestream- \_ \_ Inhaltstyp Attribut im Bytestream**](mf-bytestream-content-type-attribute.md) verfügbar.

Fügen Sie zum Registrieren eines neuen bytestreamhandlers einen Eintrag hinzu, dessen Name die CLSID des Handlers ist, in kanonischer Zeichen folgen Form. Der Wert des Eintrags ist eine Zeichenfolge (reg \_ SZ), die eine kurze Beschreibung des Handlers enthält, z. b. "My Byte-Stream Handler". Der quellresolver ruft **cokreateinstance** auf, um den Handler aus der CLSID zu erstellen. Sie können denselben Handler unter mehr als einer Erweiterung oder einem MIME-Typ registrieren.

Byte Datenstrom Handler machen die [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) -Schnittstelle verfügbar. Wenn der quellresolver einen passenden Byte Datenstrom Handler findet, wird [**IMF bytestreamhandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)aufgerufen. Bei der Eingabe für diese Methode handelt es sich um einen Zeiger auf den Bytestream Plus um die ursprüngliche URL, falls verfügbar. Der Byte Datenstrom Handler liest aus dem Bytestream, bis er genug Daten analysiert, um die Medienquelle zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresolver](source-resolver.md)
</dt> </dl>

 

 



