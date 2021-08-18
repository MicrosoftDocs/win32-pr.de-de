---
title: ServiceTask1-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Das ServiceTask1-Element stellt den ersten Aufgabenbereich des Onlineshops dar.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- ServiceTask1-Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fc22e01329728935e2953b5be7a3a1042cee00da3a3b9756915de2aeafe9b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995410"
---
# <a name="servicetask1-element"></a>ServiceTask1-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **ServiceTask1-Element** stellt den ersten Aufgabenbereich des Onlineshops dar.

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                             | BESCHREIBUNG                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)<br/> | URL für die Webseite, die Windows Media Player wird.<br/> |



 

## <a name="parentchild-elements"></a>Über- und untergeordnete Elemente



| Hierarchy       | Element                       |
|-----------------|-------------------------------|
| Übergeordnete Elemente | **ServiceInfo**               |
| Untergeordnete Elemente  | **ButtonText,** **ButtonTip** |



 

## <a name="remarks"></a>Hinweise

**ServiceTask1** wird als primärer Aufgabenbereich für kommerzielle Aktivitäten betrachtet. Es ist der Aufgabenbereich, der angezeigt wird, wenn sich der Benutzer für den Erwerb von Musik entscheidet.

> [!Note]  
> Windows Media Player 10 verfügt über drei Aufgabenbereiche, in denen ein Onlineshop seine Webseiten anzeigen kann. Der Onlineshop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich( dargestellt durch **ServiceTask1),** den der Benutzer anzeigen kann, indem er auf die **Registerkarte Onlineshops** klickt.

 

In den Aufgabenbereichen des Onlineshops wird eine einzelne Browserinstanz gemeinsam verwendet. Dies bedeutet, dass Sie keinen Skriptcode auf Ihrer Webseite schreiben sollten, von dem Sie erwarten, dass er weiterhin ausgeführt wird, wenn der Benutzer von der aktuellen Dienstaufgabe abwechselt.

Wenn der Benutzer die Aufgabenbereiche wechselt, speichert Windows Media Player URL und Sitzungscookies. Wenn der Benutzer zurück zum Aufgabenbereich wechselt, stellt der Player die URL und Cookies wieder wieder auf. Wenn sich der Benutzer für die Verwendung eines anderen Onlineshops entscheidet, werden die URL und die Sitzungsdaten gelöscht.

In der folgenden Tabelle sind die mit der URL-Anforderung gesendeten Parameter aufgeführt. Andere sind möglicherweise aus Gründen der Legacykompatibilität vorhanden.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows geografische Standort-ID. Die Standort-ID wird vom Benutzer im Bereich **Standort** der Einstellungen für regionale Optionen und Sprachoptionen in Systemsteuerung. |
| *locale*     | Windows Media Player-ID.                                                                                                                                     |
| *userlocale* | Windows-ID. Das Gebiets anders wird vom Benutzer im Bereich **Standards und Formate** der Einstellungen "Regionale Optionen" und "Sprachoptionen" in Systemsteuerung.        |
| *version*    | Windows Media Player Versionsnummer im folgenden Format: 10.0.x.xxxx oder 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





