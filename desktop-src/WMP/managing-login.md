---
title: Verwalten der Anmeldung
description: Verwalten der Anmeldung
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player Online Stores, Verwalten von Anmeldungen
- Online Stores, Verwalten von Anmeldungen
- Geben Sie 1 Online Stores ein, und verwalten Sie Anmeldungen.
- Windows Media Player Online Stores, Anmeldungen
- Online Stores, Anmeldungen
- Typ 1 Online Stores, Anmeldungen
- Windows Media Player Online Stores, standardmäßiger Anmeldevorgang
- Online Stores, Standard-Anmeldeprozess
- Typ 1 Online Stores, Standard-Anmeldeprozess
- Windows Media Player Online Stores, ABMELDEPROZESS
- Online Stores, ABMELDEPROZESS
- Typ 1 Online Stores, ABMELDEPROZESS
- standardmäßiger Anmeldevorgang
- ABMELDEPROZESS
- Anmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389886"
---
# <a name="managing-login"></a>Verwalten der Anmeldung

Windows Media Player unterstützt eine Vielzahl von Methoden, mit denen sich der Benutzer bei einem Online Store vom Typ 1 anmelden können. Der Player stellt ein Standard Dialogfeld für die Anmeldung bereit, aber der Online Shop kann eine Webseite bereitstellen, die als Alternative zum Standard Dialogfeld fungiert.

Der Benutzer kann einen Anmeldeversuch initiieren, indem er mit der Windows Media Player-Benutzeroberfläche interagiert oder mit einer Ermittlungs Seite interagiert, die im Online Store bereitgestellt wird. Wenn der Benutzer einen Anmeldeversuch durch Interaktion mit einer Ermittlungs Seite initiiert, ruft das Skript auf der Ermittlungs Seite die [externe.-Anmelde](external-attemptlogin.md) Methode auf.

Der Anmelde Zustand des Benutzers wird vom Online Store verwaltet. Wenn sich der Anmelde Zustand des Benutzers ändert, oder wenn ein Anmeldeversuch fehlschlägt, benachrichtigt das Plug-in des Online Stores Windows Media Player durch Aufrufen von [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)und übergibt dabei wmpcnloginstatechange im *Typparameter* . Der Player übergibt die Benachrichtigung an die Ermittlungs Seite, indem er das [externe. onloginchange](external-onloginchange-event.md) -Ereignis aufhebt.

Ein **onloginchange** -aufrufswert bedeutet nicht notwendigerweise, dass sich der Anmelde Zustand des Benutzers geändert hat. Dies könnte bedeuten, dass ein Anmeldeversuch fehlgeschlagen ist. Um den Anmeldestatus des Benutzers zu bestimmen, kann der **onloginchange** -Ereignishandler die [externe. userloggedin](external-userloggedin.md) -Eigenschaft überprüfen.

In den folgenden Abschnitten werden der standardmäßige Anmeldevorgang, der Alternative Anmeldevorgang und der Abmeldevorgang beschrieben.

## <a name="standard-log-in"></a>Standard Anmeldung

Der standardmäßige Anmeldevorgang umfasst die folgenden Schritte:

1.  Der Benutzer initiiert einen Anmeldeversuch, indem er mit der Windows Media Player-Benutzeroberfläche interagiert oder mit einer Ermittlungs Seite interagiert.
2.  In Windows Media Player wird ein Dialogfeld angezeigt, in dem der Benutzer zur Eingabe eines Benutzernamens und Kennworts aufgefordert wird.
3.  Wenn der Benutzer im Dialogfeld auf die Schaltfläche " **Anmelden** " klickt, ruft Windows Media Player [iwmpcontentpartner:: Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)auf, das durch das Plug-in des Online Stores implementiert wird.
4.  Das Plug-in kommuniziert mit dem Online Store und ist entweder erfolgreich oder kann nicht in den Benutzer protokolliert werden.
5.  Wenn der Anmeldeversuch erfolgreich ist, benachrichtigt das Plug-in Windows Media Player durch Aufrufen von **iwmpcontentpartnercallback:: notify** und übergibt Variant \_ true in den **boolVal** -Member des *pContext* -Parameters. Wenn der Anmeldeversuch fehlschlägt, benachrichtigt das Plug-in Windows Media Player durch Aufrufen von **iwmpcontentpartnercallback:: notify** und übergibt einen 32-Bit-Wert im **ulVal** -Member des *pContext* -Parameters. Der Spieler übergibt dann diesen 32-Bit-Wert an [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , um die URL einer Webseite zu erhalten, die den Fehler behandeln kann.

## <a name="alternative-login"></a>Alternativer Anmelde Name

Wenn das Abonnement \_ Cap- \_ altanmeldungs-Flag im Registrierungs Eintrag " **Funktionen** " für das Plug-in des Online Stores festgelegt ist, verwendet Windows Media Player nicht das Standard Dialogfeld "Anmelden". Stattdessen ruft Windows Media Player **iwmpcontentpartner:: getiteminfo** auf, um die URL einer Webseite abzurufen, die den Anmeldevorgang ausführt. Weitere Informationen zum Registrierungs Eintrag " **Funktionen** " finden Sie unter [Registrierungsschlüssel und Einträge für den Online Store des Typs 1](registry-keys-and-entries-for-a-type-1-online-store.md).

Der Player ruft " **getiteminfo** " zweimal auf: übergeben Sie "g \_ sziteminfo \_ altloginurl", um die URL der Anmelde Webseite abzurufen, und übergeben Sie "g \_ sziteminfo \_ altlogincaption", um die Beschriftung für das Fenster abzurufen, das die Webseite hostet. Wenn **getiteminfo** die URL der Anmelde Webseite zurückgibt, kann Sie die Größe des Anmelde Fensters angeben, indem die folgende Parameter Zeichenfolge an die URL angehängt wird:

? Dlgx =*Width*&dlgy =*height*

In der Parameter Zeichenfolge sind " *Width* " und " *height* " die Breite und Höhe des Fensters in Pixel. Beispielsweise könnte **getiteminfo** die folgende Zeichenfolge zurückgeben, um anzugeben, dass AltLogin.htm in einem Fenster mit einer Breite von 800 Pixeln und einer Höhe von 400 Pixel angezeigt werden soll.


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



Der Alternative Anmeldevorgang umfasst die folgenden Schritte:

1.  Der Benutzer initiiert einen Anmeldeversuch, indem er mit der Windows Media Player-Benutzeroberfläche interagiert oder mit einer Ermittlungs Seite interagiert.
2.  Windows Media Player öffnet ein modales Fenster, in dem die vom Online Store bereitgestellte Anmelde Webseite angezeigt wird.
3.  Die Webseite kommuniziert mit dem Online Store und ist entweder erfolgreich oder kann nicht in den Benutzer protokolliert werden.
4.  Wenn der Anmeldeversuch erfolgreich ist, benachrichtigt die Webseite das Plug-in des Online Stores durch Aufrufen von " [extern. SendMessage](external-sendmessage.md)", was zu einem Aufruf von " [iwmpcontentpartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)" führt. Das Plug-in für den Online Store ermittelt, dass der Anmeldeversuch erfolgreich war, indem er die an **iwmpcontentpartner:: SendMessage** über gebenden Parameter überprüft. Diese Parameter werden von Windows Media Player nicht interpretiert. Sie sind nur für den Online Shop von Bedeutung. Das Plug-in ruft **iwmpcontentpartnercallback:: notify** auf und übergibt Variant \_ true im **boolVal** -Member des *pContext* -Parameters. Wenn bei der Anmeldung ein Fehler auftritt, muss der Online Shop festlegen, wie der Benutzer unterstützt werden soll. Eine Möglichkeit besteht darin, eine neue Webseite im modalen Fenster anzuzeigen, das die Alternative Anmelde Webseite hostet.

## <a name="log-out"></a>Abmelden

Der Abmeldevorgang umfasst die folgenden Schritte.

1.  Der Benutzer initiiert einen Abmelde Versuch durch Interaktion mit der Windows Media Player-Benutzeroberfläche oder durch interagieren mit einer Suchseite.
2.  Windows Media Player ruft [iwmpcontentpartner:: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)auf, das durch das Plug-in des Online Stores implementiert wird.
3.  Das Plug-in kommuniziert mit dem Online Store und ist entweder erfolgreich oder kann den Benutzer nicht abmelden.
4.  Wenn der Abmelde Versuch erfolgreich ist, benachrichtigt das Plug-in Windows Media Player durch Aufrufen von **iwmpcontentpartnercallback:: notify** und übergibt Variant \_ false im **boolVal** -Member des *pContext* -Parameters.

Wenn ein Anmeldeversuch erfolgreich war, ruft das Plug-in des Online Stores **iwmpcontentpartnercallback:: notify** auf und übergibt dabei wmpcnloginstatechange im *Typparameter* . Das Plug-in verwendet den *pContext* -Parameter, um den aktuellen Anmelde Zustand des Benutzers anzugeben. Wenn das Plug-in *pContext* -> **boolVal** auf Variant \_ true festlegt, wird der Benutzer angemeldet. Wenn das Plug-in *pContext* -> **boolVal** auf Variant \_ false festlegt, wird der Benutzer abgemeldet. Beachten Sie, dass *pContext* nicht angibt, ob der Versuch erfolgreich war oder fehlgeschlagen ist. Stattdessen gibt Sie den aktuellen Anmelde Zustand des Benutzers an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Extern.-Anmelde Name**](external-attemptlogin.md)
</dt> <dt>

[**Externes. onloginchange-Ereignis**](external-onloginchange-event.md)
</dt> <dt>

[**Extern. userloggedin**](external-userloggedin.md)
</dt> <dt>

[**Iwmpcontentpartner:: Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Iwmpcontentpartner:: Logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




