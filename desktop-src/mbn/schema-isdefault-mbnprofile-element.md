---
description: Gibt an, ob dies das Standardprofil für das Gerät ist.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: IsDefault-Element (mbnprofile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484827"
---
# <a name="isdefault-mbnprofile-element"></a>IsDefault-Element (mbnprofile)

Das **IsDefault (mbnprofile)** -Element gibt an, ob dies das Standardprofil für das Gerät ist.

Dies ist ein optionales Element, und wenn es nicht angegeben ist, wird das Profil nicht als Standardprofil festgelegt.

Das Standardprofil wird vom mobilen Breitbanddienst für folgende Zwecke verwendet:

-   Der Mobile Breitbanddienst verwendet beim Ausführen automatischer Netzwerkverbindungen die Verbindungseinstellungen des Standard Profils. Diese Einstellungen umfassen Zugriffspunkt Name, Benutzername, Kennwort usw.
-   Die automatische Verbindungsrichtlinie für ein mobiles Breitband Gerät stammt aus dem Standardprofil.
-   Die Benutzeroberfläche für die Netzwerkverbindung des Betriebssystems verwendet auch Verbindungsdaten aus dem Standardprofil für Verbindungs Vorgänge.

Mobil Funk Dienstanbieter können die Verbindungsdetails in einem Profil bereitstellen und dieses Profil als Standardprofil konfigurieren. Der Mobile Breitbanddienst verwendet diese Verbindungseinstellungen, ohne dass der Benutzer zur Eingabe aufgefordert wird.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

Das **IsDefault** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.

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

 

 




