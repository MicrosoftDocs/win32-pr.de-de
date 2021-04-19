---
title: Servicinput info-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das servicinput info-Element ist das Hauptelement für das ServiceInfo.xml Dokument.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Servicinput info-Element, Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361917"
---
# <a name="serviceinfo-element"></a>Servicinput info-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **servicinput Info** -Element ist das Hauptelement für das ServiceInfo.xml Dokument.

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
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)<br/> | Die Version der ServiceInfo.xml Datei. Version 1,00 wird für Windows Media Player unterstützt.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Schlüssel** (erforderlich)<br/>                 | Die Dienst Schlüssel Zeichenfolge, die den Online Store eindeutig identifiziert.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**Contentpartner**<br/>                 | Gibt an, ob der Online Shop ein Typ-1-Speicher ist. Der Wert "true" gibt an, dass der Speicher ein Typ-1-Speicher ist. Der Wert "false" gibt an, dass es sich bei dem Speicher nicht um einen Speicher vom Typ 1 handelt. Das heißt, es handelt sich um einen Speicher vom Typ 2. Der Standardwert ist FALSE.<br/> |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente | Keine                                                                                                                                                                               |
| Untergeordnete Elemente  | **Albuminfo**, **buycd**, **Color**, **Description**, **FriendlyName**, **HtmlView**, **Image**, **Infocenter**, **install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |



 

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert. Andere können für Legacy Kompatibilitätszwecke vorhanden sein. Die Anforderung enthält auch alle Parameter, die Sie mithilfe des Befehlszeilen Parameters "serviceextra" von Windows Media Player Setup angegeben haben.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | ID des geografischen Standorts für Windows. Die Speicherort-ID wird vom Benutzer im Bereich **Speicherort** der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben. |
| *locale*     | Windows Media Player-Gebiets Schema-ID.                                                                                                                                     |
| *UserLocale* | Windows-Gebiets Schema-ID. Das Gebiets Schema wird vom Benutzer im Bereich " **Standards und Formate** " der Einstellungen für Regions-und Sprachoptionen in der Systemsteuerung angegeben.        |
| *version*    | Windows Media Player-Versionsnummer im folgenden Format: 10.0. x. xxxx oder 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





