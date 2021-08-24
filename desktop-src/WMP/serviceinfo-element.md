---
title: ServiceInfo-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Das ServiceInfo-Element ist das Hauptelement für das ServiceInfo.xml Dokument.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- ServiceInfo-Element Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b3be774d019555daa75b78edf6a7ed76351e7523712313365dd6c80bfee7cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763640"
---
# <a name="serviceinfo-element"></a>ServiceInfo-Element

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **ServiceInfo-Element** ist das Hauptelement für das ServiceInfo.xml Dokument.

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)<br/> | Version der ServiceInfo.xml-Datei. Version 1.00 wird für Windows Media Player unterstützt.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Schlüssel** (erforderlich)<br/>                 | Die Dienstschlüsselzeichenfolge, die den Onlineshop eindeutig identifiziert.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | Gibt an, ob der Onlineshop ein Store vom Typ 1 ist. Der Wert "true" gibt an, dass der Speicher ein Speicher vom Typ 1 ist. Der Wert "false" gibt an, dass der Speicher kein Speicher vom Typ 1 ist. Das heißt, es handelt sich um einen Speicher vom Typ 2. Der Standardwert ist FALSE.<br/> |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente | Keine                                                                                                                                                                               |
| Untergeordnete Elemente  | **AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |



 

## <a name="remarks"></a>Hinweise

In der folgenden Tabelle sind die Parameter aufgeführt, die mit der URL-Anforderung gesendet werden. Andere sind möglicherweise aus Gründen der Legacykompatibilität vorhanden. Die Anforderung enthält auch alle Parameter, die Sie mithilfe des ServiceExtra-Befehlszeilenparameters von Windows Media Player Setup angegeben haben.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows ID des geografischen Standorts. Die Standort-ID wird vom Benutzer im Bereich **Standort** der Einstellungen Regional und Sprachoptionen in Systemsteuerung angegeben. |
| *locale*     | Windows Media Player Gebietsschema-ID.                                                                                                                                     |
| *userlocale* | Windows Gebietsschema-ID. Das Gebietsschema wird vom Benutzer im Bereich **Standards und Formate** der Einstellungen regional und Sprachoptionen in Systemsteuerung angegeben.        |
| *version*    | Windows Media Player Versionsnummer im folgenden Format: 10.0.x.xxxx oder 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





