---
title: ServiceTask3-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das ServiceTask3-Element stellt den dritten Aufgabenbereich im Online Store dar.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- ServiceTask3-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d78b9e70c7e6933693f4d29750e9e3c0b4e897a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362139"
---
# <a name="servicetask3-element"></a>ServiceTask3-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **ServiceTask3** -Element stellt den dritten Aufgabenbereich im Online Store dar.

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                             | BESCHREIBUNG                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)<br/> | Die URL für die Webseite, die von Windows Media Player angezeigt wird.<br/> |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element                       |
|-----------------|-------------------------------|
| Übergeordnete Elemente | **ServiceInfo**               |
| Untergeordnete Elemente  | **ButtonText**, **buttontip** |



 

## <a name="remarks"></a>Bemerkungen

**ServiceTask1** wird als primärer Aufgabenbereich für die Teilnahme an kommerziellen Aktivitäten angesehen. Dies ist der Aufgabenbereich, der angezeigt wird, wenn der Benutzer sich für den Kauf von Musik entscheidet. Verwenden Sie **ServiceTask3** für andere Online Store-Aktivitäten.

> [!Note]  
> Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann. Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer durch Klicken auf die Registerkarte " **Online Stores** " anzeigen kann. die **ServiceTask2** -und **ServiceTask3** -Elemente werden von Windows Media Player 11 ignoriert.

 

Online Store-Aufgabenbereiche nutzen eine einzelne Browser Instanz gemeinsam. Dies bedeutet, dass Sie auf Ihrer Webseite keinen Skriptcode schreiben sollten, der fortgesetzt werden soll, wenn der Benutzer von der aktuellen Dienst Aufgabe abwechselt.

Wenn der Benutzer Aufgabenbereiche wechselt, werden die URL-und Sitzungs Cookies in Windows Media Player gespeichert. Wenn der Benutzer wieder zum Aufgabenbereich wechselt, stellt der Spieler die URL und Cookies wieder her. Wenn sich der Benutzer für die Verwendung eines anderen Online Stores entscheidet, werden die URL-und Sitzungsdaten gelöscht.

In der folgenden Tabelle werden die mit der URL-Anforderung gesendeten Parameter ausführlich erläutert.



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

 

 





