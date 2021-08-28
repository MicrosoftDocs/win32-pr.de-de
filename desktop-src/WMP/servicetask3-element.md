---
title: ServiceTask3-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Das ServiceTask3-Element stellt den dritten Aufgabenbereich des Onlineshops dar.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- ServiceTask3-Element Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c53ef9eb4a758e47d639446750465934fb4a6c031d8abd387276add2f0df519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763630"
---
# <a name="servicetask3-element"></a>ServiceTask3-Element

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **ServiceTask3-Element** stellt den dritten Aufgabenbereich des Onlineshops dar.

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                             | BESCHREIBUNG                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)<br/> | URL für die Webseite, die Windows Media Player angezeigt wird.<br/> |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element                       |
|-----------------|-------------------------------|
| Übergeordnete Elemente | **ServiceInfo**               |
| Untergeordnete Elemente  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Hinweise

**ServiceTask1** wird als primärer Aufgabenbereich für kommerzielle Aktivitäten betrachtet. Es ist der Aufgabenbereich, der angezeigt wird, wenn der Benutzer Musik kaufen möchte. Verwenden Sie **ServiceTask3** für andere Aktivitäten im Onlineshop.

> [!Note]  
> Windows Media Player 10 verfügt über drei Aufgabenbereiche, in denen ein Onlineshop seine Webseiten anzeigen kann. Der Onlineshop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer anzeigen kann, indem er auf die Registerkarte **Onlineshops** klickt. Windows Media Player 11 ignoriert die Elemente **ServiceTask2** und **ServiceTask3.**

 

In Den Aufgabenbereichen von Onlineshops wird eine einzelne Browserinstanz gemeinsam verwendet. Dies bedeutet, dass Sie auf Ihrer Webseite keinen Skriptcode schreiben sollten, der weiterhin ausgeführt werden soll, wenn der Benutzer von der aktuellen Dienstaufgabe abschaltet.

Wenn der Benutzer den Aufgabenbereich wechselt, speichert Windows Media Player die URL und Sitzungscookies. Wenn der Benutzer zurück zum Aufgabenbereich wechselt, stellt der Player die URL und die Cookies wieder her. Wenn der Benutzer einen anderen Onlineshop verwendet, werden die URL- und Sitzungsdaten gelöscht.

In der folgenden Tabelle sind die Parameter aufgeführt, die mit der URL-Anforderung gesendet werden.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows ID des geografischen Standorts. Die Standort-ID wird vom Benutzer im Bereich **Standort** der Einstellungen Regional and Language Options (Regions- und Sprachoptionen) in Systemsteuerung angegeben. |
| *locale*     | Windows Media Player Gebietsschema-ID.                                                                                                                                     |
| *userlocale* | Windows Gebietsschema-ID. Das Gebietsschema wird vom Benutzer im Bereich **Standards und Formate** der Einstellungen regional und Sprachoptionen in Systemsteuerung angegeben.        |
| *version*    | Windows Media Player Versionsnummer im folgenden Format: 10.0.x.xxxx oder 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





