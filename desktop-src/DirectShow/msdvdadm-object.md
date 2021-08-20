---
description: MSDVDAdm-Objekt
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: MSDVDAdm-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4001def80bff94920996dc627869ffecfd6dda3fbc679be79f2b321ac33a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072974"
---
# <a name="msdvdadm-object"></a>MSDVDAdm-Objekt

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

> [!Note]  
> Diese API ist veraltet. Informationen zur Wiedergabe und Navigation von DVD in DirectShow finden Sie unter [DVD-Anwendungen](dvd-applications.md).

 

Mit den Methoden und Eigenschaften des Verwaltungsobjekts kann eine Skriptanwendung ihre Standardeinstellungen in der `MSDVDAdm` Microsoft® Windows® ändern. Die Registrierung ist eine Datenbank auf allen Windows, in denen Anwendungen Informationen über sich selbst speichern können, die bei der Initialisierung oder zur Laufzeit verwendet werden sollen.

Die meisten dieser Methoden und Eigenschaften legen die aktuellen Werte im [MSWebDVD-Objekt](mswebdvd-object.md) selbst nicht fest oder rufen sie ab. Dies bedeutet beispielsweise, dass beim Aufrufen von **GetParentalLevel** der zurückgegebene Wert nicht die aktuelle im -Objekt gespeicherte Jugendebene ist. Es handelt sich vielmehr um die in der Registrierung gespeicherte Standardebene der Eltern. Um die aktuelle Jugendstufe zu erhalten, rufen Sie die **MSWebDVD-Methode** [**GetPlayerParentalLevel auf.**](getplayerparentallevel-method.md) Beim [**Aufrufen von SaveParentalLevel**](saveparentallevel-method.md) wird einfach eine neue Standardzugriffsebene für Eltern in die Registrierung schreibt. Sie müssen weiterhin die **MSWebDVD-Methode** [**SelectParentalLevel**](selectparentallevel-method.md) aufrufen, damit die Änderung sofort im **MSWebDVD-Objekt wirksam** wird. Die LCID-Standardmethoden (Locale Identifier) funktionieren auf ähnliche Weise.

Andererseits werden die [**Methoden BookmarkOnStop**](bookmarkonstop-property.md) und [**BookmarkOnClose**](bookmarkonclose-property.md) sofort wirksam, da das **MSWebDVD-Objekt** diese Einstellungen überprüft, unmittelbar bevor der Benutzer die Wiedergabe beendet oder die Anwendung schließt, anstatt während der Initialisierung.

Sie greifen über `MSDVDAdm` die **DVDAdm-Eigenschaft** von **MSWebDVD auf das -Objekt zu.** Wenn das **MSWebDVD-Objekt** also beispielsweise "DVD" heißt, rufen Sie **ChangePassword** auf, wie im folgenden Codebeispiel gezeigt.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Methoden und Eigenschaften**

In der folgenden Tabelle sind die Methoden und Eigenschaften aufgeführt, die von den MSDVDAdm-Objektmethoden und -Eigenschaften verfügbar gemacht werden.



| Methode                                                          | Beschreibung                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Speichert ein neues Anwendungskennwort in der Registrierung.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Speichert eine neue Standardmäßige Jugendstufe in der Registrierung.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Speichert das neue Land bzw. die Neue Elternregion der Anwendung in der Registrierung.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Testet, ob das angegebene Kennwort dem zuvor gespeicherten Kennwort entspricht.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Ruft die Ebene der Eltern ab, die zuletzt in der Registrierung gespeichert wurde.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Ruft das Land/die Region der Eltern ab, das/die zuletzt in der Registrierung gespeichert wurde.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Stellt die Einstellungen des Systembildschirmschoners wieder auf.                                                                                                                                       |
| Eigenschaft                                                        | Beschreibung                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Schaltet den Systembildschirmschoner ein oder aus.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Legt die Registrierungseinstellung für die vom Benutzer angegebene Standard-LCID für den Audiostream fest oder ruft sie ab.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Legt die Registrierungseinstellung für die vom Benutzer angegebene Standard-LCID für den Unterbilddatenstrom fest oder ruft sie ab.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Legt die Registrierungseinstellung für die vom Benutzer angegebene Standard-LCID für Menüs fest oder ruft sie ab.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Legt einen Wert fest oder ruft einen Wert ab, der das MSDVDAdm-Objekt darüber informiert, ob ein Lesezeichen des aktuellen Speicherorts und der aktuellen Einstellungen automatisch gespeichert werden soll, wenn der Benutzer auf die **Schaltfläche Beenden** klickt. |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Legt einen Wert fest oder ruft einen Wert ab, der das MSDVDAdm-Objekt darüber informiert, ob ein Lesezeichen des aktuellen Speicherorts und der aktuellen Einstellungen automatisch gespeichert werden soll, wenn der Benutzer die Anwendung schließt.     |



 

 

 



