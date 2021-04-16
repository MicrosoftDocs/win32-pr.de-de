---
description: Benutzeroberflächen Objekte unterstützen nur ein Handle pro Objekt. Prozesse können keine Handles für Benutzer Objekte erben oder duplizieren. Prozesse in einer Sitzung können nicht auf ein Benutzer Handle in einer anderen Sitzung verweisen.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Benutzerobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ed8afcf0f1d0e4c232cf503bc2c7ba86dca42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551379"
---
# <a name="user-objects"></a>Benutzerobjekte

Benutzeroberflächen Objekte unterstützen nur ein Handle pro Objekt. Prozesse können keine Handles für Benutzer Objekte erben oder duplizieren. Prozesse in einer Sitzung können nicht auf ein Benutzer Handle in einer anderen Sitzung verweisen.

Es gibt eine theoretische Grenze von 65.536 Benutzer Handles pro Sitzung. Allerdings ist die maximale Anzahl von Benutzer Handles, die pro Sitzung geöffnet werden können, in der Regel niedriger, da der verfügbare Arbeitsspeicher davon betroffen ist. Es gibt auch eine Standardeinstellung für den pro-Prozess-Grenzwert von Benutzer Handles. Legen Sie den folgenden Registrierungs Wert fest, um diesen Grenzwert zu ändern:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **userprocesshandlequota**

Dieser Wert kann auf eine Zahl zwischen 200 und 18.000 festgelegt werden.

## <a name="handles-to-user-objects"></a>Handles für Benutzer Objekte

Handles für Benutzer Objekte sind für alle Prozesse öffentlich. Das heißt, jeder Prozess kann das Benutzerobjekt Handle verwenden, vorausgesetzt, dass der Prozess über Sicherheits Zugriff auf das Objekt verfügt.

In der folgenden Abbildung erstellt eine Anwendung ein Window-Objekt. Die Funktion " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " erstellt das Fenster Objekt und gibt ein Objekt Handle zurück.

![Anwendung, die ein Fenster Objekt erstellt](images/cshob-01.png)

Nachdem das Fenster Objekt erstellt wurde, kann die Anwendung das Fenster Handle verwenden, um das Fenster anzuzeigen oder zu ändern. Das Handle bleibt gültig, bis das Fenster Objekt zerstört wird.

In der nächsten Abbildung zerstört die Anwendung das Window-Objekt. Die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion entfernt das Window-Objekt aus dem Arbeitsspeicher, wodurch das Fenster Handle ungültig wird.

![zerstören eines Fenster Objekts](images/cshob-02.png)

## <a name="managing-user-objects"></a>Verwalten von Benutzer Objekten

In der folgenden Tabelle werden die Benutzer Objekte sowie die Ersteller-und Zerstörungs Funktionen der einzelnen Objekte aufgelistet. Die Ersteller-Funktionen erstellen entweder das-Objekt und ein-Objekt Handle oder geben einfach das vorhandene Objekt Handle zurück. Die zerstörerfunktionen entfernen das Objekt aus dem Arbeitsspeicher, wodurch das Objekt Handle ungültig wird.



| Benutzerobjekt       | Creator-Funktion                                                                                                                                                                                                                                                              | Destroyer-Funktion                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Zugriffstasten Tabelle | [**"Kreateacceleratortable"**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Einfügemarke             | [**Auflistungs Daten Satz**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursor            | " [**Kreatecursor**](/windows/win32/api/winuser/nf-winuser-createcursor)", " [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)", " [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) "                                                                                                                                                   | [**Destroycursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| DDE-Konversation  | [**DDE Connect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DDE ConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DDE Disconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DDE disconnectlist**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Hook              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**Unhuokwindowshookex**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Symbol              | " [**Kreateikonindirekt**](/windows/win32/api/winuser/nf-winuser-createiconindirect)", " [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)", " [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) "                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menü              | " [**Anatemenu**](/windows/win32/api/winuser/nf-winuser-createmenu)", " [**kreatepopupmenu**](/windows/win32/api/winuser/nf-winuser-createpopupmenu)", " [**loadmenu**](/windows/win32/api/winuser/nf-winuser-loadmenua)", " [**loadmenuindirekte**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta) "                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Fenster            | " [**Kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)", " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)", " [**kreatedialogparam**](/windows/win32/api/winuser/nf-winuser-createdialogparama)", " [**kreatedialogindirectparam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)", " [**anatemdiwindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) " | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Fensterposition   | [**Begindeferwindowpos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**Enddeferwindowpos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
