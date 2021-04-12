---
title: Ausschalten der Rückruf Sicherheit
description: Die Sicherheitseinstellungen für Anrufe bestimmen, ob ein Client über die Berechtigung verfügt, die Methoden eines Servers aufzurufen. Es gibt zwei Möglichkeiten, die Aufruf Sicherheit zu deaktivieren. dazu gehört das Verwenden von Dcomcnfg.exe, um die Registrierung zu ändern, und das andere erfordert Aufrufe von CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388082"
---
# <a name="turning-off-call-security"></a>Ausschalten der Rückruf Sicherheit

Die Sicherheitseinstellungen für Anrufe bestimmen, ob ein Client über die Berechtigung verfügt, die Methoden eines Servers aufzurufen. Es gibt zwei Möglichkeiten, die Aufruf Sicherheit zu deaktivieren: eine erfordert die Verwendung von Dcomcnfg.exe, um die Registrierung zu ändern, und die andere erfordert Aufrufe von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Ausschalten der Rückruf Sicherheit mithilfe von DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Programm gesteuertes Ausschalten der Rückruf Sicherheit](#turning-off-call-security-programmatically)
-   [Zugehörige Themen](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Ausschalten der Rückruf Sicherheit mithilfe von DCOMCNFG

Die aufrufssicherheit kann am einfachsten mithilfe Dcomcnfg.exe deaktiviert werden, um die Registrierung zu ändern. Die Verwendung Dcomcnfg.exe zum Ausschalten der Sicherheit funktioniert jedoch nur, wenn sowohl der Client als auch der Server [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufruft. Dies liegt daran, dass beim Aufrufen von **CoInitializeSecurity** die Registrierungs Einstellungen von DCOM ignoriert werden und stattdessen die für **CoInitializeSecurity** bereitgestellten Werte verwendet werden.

Zum Deaktivieren der Sicherheit mit Dcomcnfg.exe müssen sowohl der Client als auch der Server die Authentifizierungs Ebenen auf keine festlegen. Die folgenden Schritte müssen ausgeführt werden:

1.  Führen Sie "Dcomcnfg.exe" aus.
2.  Wählen Sie auf der Seite **Anwendungen** die Anwendung aus, die den Server darstellt. Klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).
3.  Klicken Sie auf die Registerkarte **Allgemein**.
4.  Wählen Sie im Listenfeld **Standard Authentifizierungs Ebene** die Option **(keine)** aus.
5.  Klicken Sie auf die Schaltfläche **anwenden** , um die Änderungen anzuwenden Änderungen werden jedoch nicht auf alle laufenden Instanzen der Anwendung angewendet.
6.  Wenn der Client in der Liste auf der Seite *Anwendungen* angezeigt wird, wiederholen Sie die Schritte 2 bis 5, und wählen Sie den Client anstelle des Servers für Schritt 2 aus. Klicken Sie dann auf die Schaltfläche **OK**. Wenn der Client nicht in der Liste enthalten ist, können Sie eine der folgenden drei Schritte ausführen:
    -   Mithilfe von Dcomcnfg.exe können Sie die Authentifizierungs Ebene des Clients auf Computer Ebene auf keine festlegen. (Siehe die Warnung und das Verfahren weiter unten.)
    -   Sie können die Authentifizierungs Ebene des Clients Programm gesteuert auf "None" festlegen.
    -   Sie können einen [AppID](appid-key.md) -Schlüssel für den Client erstellen, um die Authentifizierungs Ebene "None" anzugeben. (Siehe [festlegen Process-Wide Sicherheit über die Registrierung](setting-processwide-security-through-the-registry.md).)

So legen Sie die Authentifizierungs Ebene auf der Computer weiten Basis auf "None" fest:

> [!Note]  
> Das Festlegen der Computer weiten Authentifizierungs Ebene auf None ist äußerst unsicher.

 

1.  Führen Sie "Dcomcnfg.exe" aus.
2.  Wählen Sie die Registerkarte **Standardeigenschaften** aus.
3.  Wählen Sie im Listenfeld **Standard Authentifizierungs Ebene** die Option **(keine)** aus.
4.  Klicken Sie auf die Schaltfläche **OK** .

## <a name="turning-off-call-security-programmatically"></a>Programm gesteuertes Ausschalten der Rückruf Sicherheit

Um die Aufruf Sicherheit Programm gesteuert zu aktivieren, müssen sowohl der Client als auch der Server **CoInitializeSecurity** aufrufen und die Authentifizierungs Ebene im Parameter *dwauthnlevel* auf RPC \_ C \_ authn \_ Level \_ None festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deaktivieren der Aktivierungs Sicherheit](turning-off-activation-security.md)
</dt> </dl>

 

 




