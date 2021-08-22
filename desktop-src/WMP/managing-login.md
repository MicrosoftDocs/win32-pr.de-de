---
title: Verwalten der Anmeldung
description: Verwalten der Anmeldung
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player Onlineshops, Verwalten von Anmeldungen
- Onlineshops, Verwalten von Anmeldungen
- Geben Sie 1 Onlineshops ein, verwalten Sie Anmeldungen.
- Windows Media Player Onlineshops,Anmeldungen
- Onlineshops, Anmeldungen
- Geben Sie 1 Onlineshops und Anmeldungen ein.
- Windows Media Player Onlineshops, Standard-Anmeldevorgang
- Onlineshops, Standard-Anmeldevorgang
- Geben Sie 1 Onlineshops ein, Standard-Anmeldevorgang
- Windows Media Player Onlineshops, Abmeldungsprozess
- Onlineshops, Abmeldungsprozess
- Geben Sie 1 Onlineshops ein, abmelden Sie sich.
- Standard-Anmeldevorgang
- Abmeldungsprozess
- Anmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698385f2d5a618899bd4fe440db5a552859c7647ceb2ae11e02b773c96479d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135173"
---
# <a name="managing-login"></a>Verwalten der Anmeldung

Windows Media Player unterstützt eine Vielzahl von Methoden, mit der sich der Benutzer bei einem Onlineshop vom Typ 1 anmelden kann. Der Player stellt ein Standarddialogfeld für die Anmeldung bereit, aber der Onlineshop kann eine Webseite bereitstellen, die als Alternative zum Standarddialogfeld dient.

Der Benutzer kann einen Anmeldeversuch initiieren, indem er mit der Windows Media Player Benutzeroberfläche interagiert oder mit einer vom Onlineshop bereitgestellten Ermittlungsseite interagiert. Wenn der Benutzer einen Anmeldeversuch initiiert, indem er mit einer Ermittlungsseite interagiert, ruft das Skript auf der Ermittlungsseite die [External.attemptLogin-Methode](external-attemptlogin.md) auf.

Der Anmeldestatus des Benutzers wird vom Onlineshop verwaltet. Wenn sich der Anmeldezustand des Benutzers ändert oder ein Anmeldeversuch fehlschlägt, benachrichtigt das Plug-In des Onlineshops Windows Media Player, indem [es IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)aufruft und wmpcnLoginStateChange im *Typparameter* übergibt. Der Player übergibt die Benachrichtigung an die Ermittlungsseite, indem er das [External.OnLoginChange-Ereignis](external-onloginchange-event.md) ausgibt.

Ein Aufruf von **OnLoginChange** bedeutet nicht notwendigerweise, dass sich der Anmeldezustand des Benutzers geändert hat. dies kann bedeuten, dass ein Anmeldeversuch fehlgeschlagen ist. Um den Anmeldezustand des Benutzers zu bestimmen, kann der **OnLoginChange-Ereignishandler** die [External.userLoggedIn-Eigenschaft](external-userloggedin.md) überprüfen.

In den folgenden Abschnitten werden der Standardprotokollierungsprozess, der alternative Anmeldevorgang und der Abmeldungsprozess beschrieben.

## <a name="standard-log-in"></a>Standardanmeldung

Der Standardprotokollierungsprozess umfasst die folgenden Schritte:

1.  Der Benutzer initiiert einen Anmeldeversuch, indem er mit der Windows Media Player Benutzeroberfläche interagiert oder mit einer Ermittlungsseite interagiert.
2.  Windows Media Player zeigt ein Dialogfeld an, in dem der Benutzer zur Eingabe eines Benutzernamens und Kennworts aufgefordert wird.
3.  Wenn der Benutzer im Dialogfeld auf die Schaltfläche **Anmelden** klickt, ruft Windows Media Player [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)auf, das vom Plug-In des Onlineshops implementiert wird.
4.  Das Plug-In kommuniziert mit dem Onlineshop und kann sich entweder erfolgreich oder nicht beim Benutzer anmelden.
5.  Wenn der Anmeldeversuch erfolgreich ist, benachrichtigt das Plug-In Windows Media Player, indem **es IWMPContentPartnerCallback::Notify** aufruft und VARIANT \_ TRUE im **boolVal-Member** des *pContext-Parameters* übergibt. Wenn der Anmeldeversuch fehlschlägt, benachrichtigt das Plug-In Windows Media Player durch Aufrufen von **IWMPContentPartnerCallback::Notify** und übergibt einen 32-Bit-Wert im **ulVal-Member** des *pContext-Parameters.* Der Player übergibt diesen 32-Bit-Wert dann an [IWMPContentPartner::GetItemInfo,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) um die URL einer Webseite abzurufen, die den Fehler behandeln kann.

## <a name="alternative-login"></a>Alternative Anmeldung

Wenn das \_ ABONNEMENT CAP \_ ALTLOGIN-Flag im Registrierungseintrag **Funktionen** für das Plug-In des Onlineshops festgelegt ist, verwendet Windows Media Player nicht das Standardmäßige Anmeldedialogfeld. Stattdessen ruft Windows Media Player **IWMPContentPartner::GetItemInfo** auf, um die URL einer Webseite abzurufen, die den Anmeldevorgang ausführt. Weitere Informationen zum **Registrierungseintrag Capabilities** finden Sie unter [Registrierungsschlüssel und -einträge für einen Typ 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).

Der Player ruft **GetItemInfo** zweimal auf: einmal übergibt g \_ szItemInfo \_ ALTLoginURL, um die URL der Anmeldewebseite abzurufen, und einmal g \_ szItemInfo \_ ALTLoginCaption, um die Beschriftung für das Fenster abzurufen, das die Webseite hostet. Wenn **GetItemInfo** die URL der Anmeldewebseite zurückgibt, kann die Größe des Anmeldefensters angegeben werden, indem die folgende Parameterzeichenfolge an die URL angefügt wird:

? DlgX=*Width*&DlgY=*height*

In der Parameterzeichenfolge sind *Breite* und *Höhe* die Breite und Höhe des Fensters in Pixel. **GetItemInfo** könnte beispielsweise die folgende Zeichenfolge zurückgeben, um anzugeben, dass AltLogin.htm in einem Fenster mit einer Breite von 800 Pixeln und einer Höhe von 400 Pixeln angezeigt werden soll.


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



Der alternative Anmeldevorgang umfasst die folgenden Schritte:

1.  Der Benutzer initiiert einen Anmeldeversuch, indem er mit der Windows Media Player Benutzeroberfläche interagiert oder mit einer Ermittlungsseite interagiert.
2.  Windows Media Player öffnet ein modales Fenster, in dem die vom Onlineshop bereitgestellte Anmeldewebseite angezeigt wird.
3.  Die Webseite kommuniziert mit dem Onlineshop und kann sich entweder erfolgreich oder nicht beim Benutzer anmelden.
4.  Wenn der Anmeldeversuch erfolgreich ist, benachrichtigt die Webseite das Plug-In des Onlineshops, indem [External.sendMessage](external-sendmessage.md)aufgerufen wird. Dies führt zu einem Aufruf von [IWMPContentPartner::SendMessage.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) Das Plug-In des Onlineshops bestimmt, dass der Anmeldeversuch erfolgreich war, indem die an **IWMPContentPartner::SendMessage** übergebenen Parameter überprüft werden. Diese Parameter werden von Windows Media Player nicht interpretiert. sie haben nur für den Onlineshop eine Bedeutung. Das Plug-In ruft **IWMPContentPartnerCallback::Notify** auf und übergibt VARIANT \_ TRUE im **boolVal-Member** des *pContext-Parameters.* Wenn die Anmeldung fehlschlägt, muss der Onlineshop bestimmen, wie der Benutzer unterstützt werden soll. Eine Möglichkeit besteht darin, eine neue Webseite im modalen Fenster anzuzeigen, das die alternative Anmeldewebseite hostet.

## <a name="log-out"></a>Abmelden

Der Abmeldevorgang umfasst die folgenden Schritte.

1.  Der Benutzer initiiert einen Abmeldeversuch, indem er mit der Windows Media Player Benutzeroberfläche interagiert oder mit einer Ermittlungsseite interagiert.
2.  Windows Media Player ruft [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)auf, das durch das Plug-In des Onlineshops implementiert wird.
3.  Das Plug-In kommuniziert mit dem Onlineshop und kann den Benutzer entweder erfolgreich oder nicht abmelden.
4.  Wenn der Abmeldeversuch erfolgreich ist, benachrichtigt das Plug-In Windows Media Player, indem **es IWMPContentPartnerCallback::Notify** aufruft und VARIANT \_ FALSE im **boolVal-Member** des *pContext-Parameters* übergibt.

Wenn ein Anmelde- oder Abmeldeversuch erfolgreich ist, ruft das Plug-In des Onlineshops **IWMPContentPartnerCallback::Notify** auf und übergibt wmpcnLoginStateChange im *Typparameter.* Das Plug-In verwendet den *pContext-Parameter,* um den aktuellen Anmeldezustand des Benutzers anzugeben. Wenn das Plug-In *pContext* -> **boolVal** auf VARIANT \_ TRUE festlegt, wird der Benutzer angemeldet. Wenn das Plug-In *pContext* -> **boolVal** auf VARIANT \_ FALSE festlegt, wird der Benutzer abgemeldet. Beachten Sie, dass *pContext* nicht den Erfolg oder Fehler des Versuchs angibt. stattdessen wird der aktuelle Anmeldestatus des Benutzers angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External.OnLoginChange-Ereignis**](external-onloginchange-event.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner::Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner::Logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




