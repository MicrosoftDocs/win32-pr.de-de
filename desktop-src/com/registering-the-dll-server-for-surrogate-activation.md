---
title: Registrieren des dll-Servers für die ersatzaktivierung
description: Registrieren des dll-Servers für die ersatzaktivierung
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730465"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Registrieren des dll-Servers für die ersatzaktivierung

Ein dll-Server wird unter den folgenden Bedingungen in einen Ersatzprozess geladen:

-   Es muss ein AppID-Wert angegeben werden, der unter dem CLSID-Schlüssel in der Registrierung angegeben ist, und ein entsprechender [AppID](appid-key.md) -Schlüssel.
-   Bei einem Aktivierungsbefehl ist das [**lokale CLSCTX- \_ \_ Server**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) Bit festgelegt, und der CLSID-Schlüssel gibt [LocalServer32](localserver32.md), [LocalServer](localserver.md)oder [LocalService](localservice.md)nicht an. Wenn andere **CLSCTX** -Bits festgelegt sind, wird der [**Verarbeitungs Algorithmus**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)für die in-Process-, local-oder remoteausführungsflags befolgt.
-   Der CLSID-Schlüssel enthält den [InProcServer32](inprocserver32.md) -Unterschlüssel.
-   Die im **InProcServer32** -Schlüssel angegebene Proxy-/Stub-dll ist vorhanden.
-   Der Wert von " [dllersatz](dllsurrogate.md) " ist unter dem Schlüssel " **AppID** " vorhanden.

Wenn ein **LocalServer**-, **LocalServer32**-oder **LocalService-Dienst** vorhanden ist, der angibt, dass eine exe-Datei vorhanden ist, wird der exe-Server oder-Dienst immer im Gegensatz zum Laden eines dll-Servers in einen Ersatzprozess gestartet.

Für den Ersatz der Ersatz Zeichen Aktivierung muss der benannte Wert von " **dllersatz** " angegeben werden. Die Aktivierung bezieht sich auf Aufrufe einer der folgenden Aktivierungs Funktionen:

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**Cokreateingestanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**Cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker:: bindtoken Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Um eine Instanz des vom System bereitgestellten Ersatz Zeichens zu starten, legen Sie den Wert von **dllersatz** entweder auf eine leere Zeichenfolge oder auf **null** fest. Um den Start eines benutzerdefinierten Ersatz Zeichens anzugeben, legen Sie den Wert auf den Pfad des Ersatz Zeichens fest.

Wenn sowohl [Remoteservername](remoteservername.md) als auch **dllersatz** für dieselbe AppID angegeben werden, wird der **Remoteservername** -Wert ignoriert, und der Wert **dllersatz** bewirkt eine Aktivierung auf dem lokalen Computer. Geben Sie für die Remote Ersatz Aktivierung den **Namen Remoteservername** , aber nicht **dllersatz** auf dem Client an, und geben Sie **dllersatz** auf dem Server an.

Ein dll-Server, der so konzipiert ist, dass er immer allein im eigenen Ersatzprozess ausgeführt wird, ist am besten mit einer AppID konfiguriert, die seiner CLSID entspricht. Geben Sie unter " **AppID**" einfach einen **dllersatz** -Wert mit dem Namen "-Value" und einem leeren Zeichen folgen Wert

Es empfiehlt sich, einen dll-Server zu konfigurieren, der ausschließlich in einem eigenen Ersatzprozess ausgeführt werden soll, und mehrere Clients in einem Netzwerk mit einem [runas](runas.md) -Wert zu verarbeiten, der unter dem **AppID** -Registrierungsschlüssel angegeben ist. Ob die **runas** "Interactive User" oder eine bestimmte Benutzeridentität angeben, hängt von der Benutzeroberfläche, der Sicherheit und anderen Serveranforderungen ab. Wenn ein **runas** -Wert angegeben wird, wird nur eine Instanz des Servers geladen, um alle Clients zu bedienen, unabhängig von der Identität des Clients. Konfigurieren Sie den Server auf der anderen Seite nicht mit **runas** , wenn die Absicht besteht, eine Instanz des dll-Servers als Ersatz für jede Remote Client Identität zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Server Anforderungen](dll-server-requirements.md)
</dt> <dt>

[Freigabe von Ersatz Zeichen](surrogate-sharing.md)
</dt> </dl>

 

 