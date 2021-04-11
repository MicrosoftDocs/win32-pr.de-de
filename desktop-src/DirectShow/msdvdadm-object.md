---
description: Msdvdadm-Objekt
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Msdvdadm-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193d5e46837c576c61b8bf1704ec967c1b6fc246
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123475"
---
# <a name="msdvdadm-object"></a>Msdvdadm-Objekt

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

> [!Note]  
> Diese API ist veraltet. Weitere Informationen zur DVD-Wiedergabe und-Navigation in DirectShow finden Sie unter [DVD-Anwendungen](dvd-applications.md).

 

Mit den Methoden und Eigenschaften des `MSDVDAdm` Objekts "Administration" kann eine Skript Anwendung ihre Standardeinstellungen in der Microsoft® Windows®-Registrierung ändern. Die Registrierung ist eine Datenbank auf allen Windows-Systemen, in denen Anwendungen Informationen über sich selbst speichern können, die bei der Initialisierung oder während der Laufzeit verwendet werden können.

Die meisten dieser Methoden und Eigenschaften legen die aktuellen Werte im [mswebdvd](mswebdvd-object.md) -Objekt selbst nicht fest oder rufen Sie ab. Dies bedeutet beispielsweise, dass beim Aufrufen von **getparameentallevel** der zurückgegebene Wert nicht die aktuelle Jugend Stufe ist, die im-Objekt gespeichert ist. Vielmehr handelt es sich hierbei um die in der Registrierung gespeicherte Standard-Jugend Stufe. Um die aktuelle Jugend Stufe abzurufen, nennen Sie die **mswebdvd** -Methode [**getplayeranallevel**](getplayerparentallevel-method.md). Durch den Aufruf von [**saveparameentallevel**](saveparentallevel-method.md) wird einfach eine neue standardmäßige Jugend Zugriffsebene in die Registrierung geschrieben. Sie müssen weiterhin die **mswebdvd** -Methode [**selectparamevel**](selectparentallevel-method.md) aufzurufen, damit die Änderungen sofort im **mswebdvd** -Objekt wirksam werden. Die Standardmethoden für Gebiets Schema Bezeichner (LCID) funktionieren auf ähnliche Weise.

Andererseits treten die [**bookmarkonstopp**](bookmarkonstop-property.md) -und [**bookmarkonclose**](bookmarkonclose-property.md) -Methoden sofort in Kraft, da das **mswebdvd** -Objekt diese Einstellungen überprüft, kurz bevor der Benutzer die Wiedergabe beendet oder die Anwendung schließt, anstatt Sie während der Initialisierung zu schließen.

Sie greifen `MSDVDAdm` auf das Objekt über die **dvdadm** -Eigenschaft von **mswebdvd** zu. Wenn z. b. das **mswebdvd** -Objekt den Namen "DVD" hat, wird **ChangePassword** aufgerufen, wie im folgenden Codebeispiel gezeigt.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Methoden und Eigenschaften**

In der folgenden Tabelle sind die Methoden und Eigenschaften aufgeführt, die von den Objektmethoden und Eigenschaften von msdvdadm verfügbar gemacht werden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Speichert ein neues Anwendungs Kennwort in der Registrierung.                                                                                                                                |
| [**Saveparameentallevel**](saveparentallevel-method.md)           | Speichert eine neue Standard-Jugend Stufe in der Registrierung.                                                                                                                              |
| [**Savepartalcountry**](saveparentalcountry-method.md)       | Speichert das neue Eltern Land/die Region der Anwendung in der Registrierung.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Testet, ob das angegebene Kennwort mit dem zuvor gespeicherten Kennwort übereinstimmt.                                                                                                      |
| [**Getparametriallevel**](getparentallevel-method.md)             | Ruft die Jugend Stufe ab, die zuletzt in der Registrierung gespeichert wurde.                                                                                                                |
| [**Getparametrialcountry**](getparentalcountry-method.md)         | Ruft das Eltern Land/die Region ab, das zuletzt in der Registrierung gespeichert wurde.                                                                                                       |
| [**Restoreskreensaver**](restorescreensaver-method.md)         | Stellt die Einstellungen des System Bildschirmschoners wieder her.                                                                                                                                       |
| Eigenschaft                                                        | BESCHREIBUNG                                                                                                                                                                      |
| [**Disablebildschirm**](disablescreensaver-property.md)       | Schaltet den Bildschirmschoner des Systems ein oder aus.                                                                                                                                         |
| [**Defaultaudiolcid**](defaultaudiolcid-property.md)           | Legt die Registrierungs Einstellung für die vom Benutzer angegebene Standard-LCID für den Audiostream fest oder ruft Sie ab.                                                                                 |
| [**Defaultsubpicturelcid**](defaultsubpicturelcid-property.md) | Legt die Registrierungs Einstellung für die vom Benutzer angegebene Standard-LCID für den subbildstream fest oder ruft Sie ab.                                                                            |
| [**Defaultmenulcid**](defaultmenulcid-property.md)             | Legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für Menüs fest oder ruft Sie ab.                                                                                            |
| [**Bookmarkonstoppt**](bookmarkonstop-property.md)               | Legt einen Wert fest oder Ruft einen Wert ab, der das msdvdadm-Objekt anweist, ob automatisch ein Lesezeichen der aktuellen Position und Einstellungen gespeichert werden soll, wenn der Benutzer auf die Schaltfläche **Beenden** klickt. |
| [**Bookmarkonclose**](bookmarkonclose-property.md)             | Legt einen Wert fest oder ruft ihn ab, der angibt, ob ein Lesezeichen des aktuellen Speicher Orts und der aktuellen Einstellungen automatisch gespeichert werden sollen, wenn der Benutzer die Anwendung schließt.     |



 

 

 



