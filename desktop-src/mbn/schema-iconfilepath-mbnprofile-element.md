---
description: Enthält den Pfad der Symbol Datei für die Verbindung.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Iconfilepath (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343698"
---
# <a name="iconfilepath-mbnprofile-element"></a>Iconfilepath (mbnprofile)-Element

Das **iconfilepath (mbnprofile)** -Element enthält den Pfad der Symbol Datei für die Verbindung.

Die Benutzeroberfläche für die Betriebssystem Verbindung zeigt dieses Symbol an, wenn eine Verbindung mit diesem Element hergestellt wird.

Wenn Sie den XML-Code zum Erstellen des Profils in [**der Methode "**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) Methode" von " [**imbnconnectionprofilemanager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) " übergeben, sollte dieser Pfad auf den Quell Speicherort der Symbol Datei verweisen. Bei erfolgreicher Erstellung des [**imbnconnectionprofile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) -Objekts kopiert der Mobile Breitbanddienst die Symbol Datei im internen Speicher, und der Profilpfad wird geändert, um dies widerzuspiegeln.

Die Symbol Datei sollte das BMP-Format mit einer Größe von 32 x 32 Pixel aufweisen.

Dieses Element ist eine Zeichenfolge mit einer Länge von bis zu 1024 Zeichen, die einen absoluten Dateipfad enthält.

Das-Element ist optional.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

Das **iconfilepath** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Mbnprofile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




