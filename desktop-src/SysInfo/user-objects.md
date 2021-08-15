---
description: Benutzeroberflächenobjekte unterstützen nur ein Handle pro Objekt. Prozesse können keine Handles an Benutzerobjekte erben oder duplizieren. Prozesse in einer Sitzung können nicht auf ein Benutzerhand handle in einer anderen Sitzung verweisen.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Benutzerobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c3cdb5c0927a5773bad818064442f654159fefba2b2dfa4d0cb4c08d17ff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884325"
---
# <a name="user-objects"></a>Benutzerobjekte

Benutzeroberflächenobjekte unterstützen nur ein Handle pro Objekt. Prozesse können keine Handles an Benutzerobjekte erben oder duplizieren. Prozesse in einer Sitzung können nicht auf ein Benutzerhand handle in einer anderen Sitzung verweisen.

Es gibt einen theoretischen Grenzwert von 65.536 Benutzerhandles pro Sitzung. Die maximale Anzahl von Benutzerhandles, die pro Sitzung geöffnet werden können, ist jedoch in der Regel niedriger, da sie vom verfügbaren Arbeitsspeicher betroffen ist. Es gibt auch eine Standardmäßiggrenze pro Prozess für Benutzerhandles. Legen Sie den folgenden Registrierungswert fest, um diesen Grenzwert zu ändern:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Dieser Wert kann auf eine Zahl zwischen 200 und 18.000 festgelegt werden.

## <a name="handles-to-user-objects"></a>Handles für Benutzerobjekte

Handles für Benutzerobjekte sind für alle Prozesse öffentlich. Das heißt, jeder Prozess kann das Benutzerobjekthand handle verwenden, vorausgesetzt, der Prozess hat Sicherheitszugriff auf das Objekt.

In der folgenden Abbildung erstellt eine Anwendung ein Fensterobjekt. Die [**CreateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowa) erstellt das Fensterobjekt und gibt ein Objekthand handle zurück.

![Anwendung, die ein Fensterobjekt erstellt](images/cshob-01.png)

Nachdem das Fensterobjekt erstellt wurde, kann die Anwendung das Fensterhand handle verwenden, um das Fenster anzuzeigen oder zu ändern. Das Handle bleibt gültig, bis das Fensterobjekt zerstört wird.

In der nächsten Abbildung zerstört die Anwendung das Fensterobjekt. Die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) entfernt das Fensterobjekt aus dem Arbeitsspeicher, wodurch das Fensterhandy ungültig wird.

![Zerstören eines Fensterobjekts](images/cshob-02.png)

## <a name="managing-user-objects"></a>Verwalten von Benutzerobjekten

In der folgenden Tabelle sind die Benutzerobjekte zusammen mit den Ersteller- und Zerstören-Funktionen der einzelnen Objekte aufgeführt. Die Erstellerfunktionen erstellen entweder das Objekt und ein Objekthand handle oder geben einfach das vorhandene Objekthand handle zurück. Die Zerstören-Funktionen entfernen das Objekt aus dem Arbeitsspeicher, wodurch das Objekthand handle ungültig wird.



| Benutzerobjekt       | Creator-Funktion                                                                                                                                                                                                                                                              | Destroyer-Funktion                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Zugriffstastentabelle | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Einfügemarke             | [**CreateCaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursor            | [**CreateCursor,**](/windows/win32/api/winuser/nf-winuser-createcursor) [**LoadCursor,**](/windows/win32/api/winuser/nf-winuser-loadcursora) [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| DDE-Konversation  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Hook              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Symbol              | [**CreateIconIndirect,**](/windows/win32/api/winuser/nf-winuser-createiconindirect) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menü              | [**CreateMenu,**](/windows/win32/api/winuser/nf-winuser-createmenu) [**CreatePopupMenu,**](/windows/win32/api/winuser/nf-winuser-createpopupmenu) [**LoadMenu,**](/windows/win32/api/winuser/nf-winuser-loadmenua) [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Fenster            | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**CreateDialogParam**](/windows/win32/api/winuser/nf-winuser-createdialogparama), [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama), [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Fensterposition   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
