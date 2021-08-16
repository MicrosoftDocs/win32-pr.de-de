---
description: Enthält den Pfad der Symboldatei für die Verbindung.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: ICONFilePath (MBNProfile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: ea662a7519a8705818ef502f5b797f437b0f89bee649d0bde18ce6f71b099d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035818"
---
# <a name="iconfilepath-mbnprofile-element"></a>ICONFilePath (MBNProfile)-Element

Das **ICONFilePath (MBNProfile)-Element** enthält den Pfad der Symboldatei für die Verbindung.

Auf der Benutzeroberfläche für die Betriebssystemverbindung wird dieses Symbol angezeigt, wenn eine Verbindung mit diesem Element hergestellt wird.

Wenn der XML-Code zum Erstellen des Profils in der [**CreateConnectionProfile-Methode**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) der [**IMbnConnectionProfileManager-Schnittstelle**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) übergeben wird, sollte dieser Pfad auf den Quellspeicherort der Symboldatei verweisen. Bei erfolgreicher Erstellung des [**IMbnConnectionProfile-Objekts**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) kopiert der Mobile Broadband-Dienst die Symboldatei in den internen Speicher, und der Profilpfad wird entsprechend geändert.

Die Symboldatei sollte im .bmp 32X32 Pixel-Dimension vorliegen.

Dieses Element ist eine Zeichenfolge mit einer Länge von bis zu 1024 Zeichen, die einen absoluten Dateipfad enthält.

Das -Element ist optional.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

Das **ICONFilePath-Element** wird durch das [**MBNProfile-Element**](schema-mbnprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




