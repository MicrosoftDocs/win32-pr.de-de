---
title: Deaktivieren der Anrufsicherheit
description: Die Aufrufsicherheit bestimmt, ob ein Client über die Berechtigung zum Aufrufen der Methoden eines Servers verfügt. Es gibt zwei Möglichkeiten, die Aufrufsicherheit zu deaktivieren. Eine besteht darin, Dcomcnfg.exe zum Ändern der Registrierung zu verwenden, und die andere erfordert Aufrufe von CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d8d8f4a48baed00655761e89a12f0aa84846a0a2defdc0b2e444b2bee9103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550564"
---
# <a name="turning-off-call-security"></a>Deaktivieren der Anrufsicherheit

Die Aufrufsicherheit bestimmt, ob ein Client über die Berechtigung zum Aufrufen der Methoden eines Servers verfügt. Es gibt zwei Möglichkeiten, die Aufrufsicherheit zu deaktivieren: Eine umfasst die Verwendung von Dcomcnfg.exe zum Ändern der Registrierung, und die andere erfordert Aufrufe von [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

-   [Deaktivieren der Anrufsicherheit mithilfe von DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Programmgesteuertes Deaktivieren der Anrufsicherheit](#turning-off-call-security-programmatically)
-   [Zugehörige Themen](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Deaktivieren der Anrufsicherheit mithilfe von DCOMCNFG

Die Aufrufsicherheit kann am einfachsten deaktiviert werden, indem Dcomcnfg.exe verwendet wird, um die Registrierung zu ändern. Die Verwendung von Dcomcnfg.exe zum Deaktivieren der Sicherheit funktioniert jedoch nur, wenn sowohl der Client als auch der Server [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen. Dies liegt daran, dass DCOM beim Aufruf von **CoInitializeSecurity** die Registrierungseinstellungen ignoriert und stattdessen die für **CoInitializeSecurity** angegebenen Werte verwendet.

Um die Sicherheit mit Dcomcnfg.exe zu deaktivieren, müssen sowohl der Client als auch der Server ihre Authentifizierungsebenen auf Keine festlegen. Die folgenden Schritte müssen ausgeführt werden:

1.  Führen Sie "Dcomcnfg.exe" aus.
2.  Wählen Sie auf der Seite **Anwendungen** die Anwendung aus, die den Server darstellt. Klicken Sie auf die Schaltfläche **Eigenschaften** (oder doppelklicken Sie auf die ausgewählte Anwendung).
3.  Klicken Sie auf die Registerkarte **Allgemein**.
4.  Wählen Sie im Listenfeld **Standardauthentifizierungsebene** die Option **(Keine)** aus.
5.  Klicken Sie auf die Schaltfläche **Übernehmen,** um die Änderungen zu übernehmen. Änderungen werden jedoch nicht auf ausgeführte Instanzen der Anwendung angewendet.
6.  Wenn der Client in der Liste auf der Seite *Anwendungen* angezeigt wird, wiederholen Sie die Schritte 2 bis 5, und wählen Sie den Client anstelle des Servers für Schritt 2 aus. Klicken Sie dann auf die Schaltfläche **OK**. Wenn der Client nicht in der Liste enthalten ist, können Sie eine der folgenden drei Schritte ausführen:
    -   Sie können die Authentifizierungsebene des Clients computerweit auf Keine festlegen, indem Sie Dcomcnfg.exe verwenden. (Weitere Informationen finden Sie in der Warnung und im folgenden Verfahren.)
    -   Sie können die Authentifizierungsebene des Clients programmgesteuert auf Keine festlegen.
    -   Sie können einen [AppID-Schlüssel](appid-key.md) für den Client erstellen, um die Authentifizierungsebene None anzugeben. (Weitere Informationen finden Sie unter [Festlegen Process-Wide Sicherheit über die Registrierung.)](setting-processwide-security-through-the-registry.md)

So legen Sie die Authentifizierungsebene computerweit auf Keine fest:

> [!Note]  
> Das Festlegen der computerweiten Authentifizierungsebene auf Keine ist äußerst unsicher.

 

1.  Führen Sie "Dcomcnfg.exe" aus.
2.  Wählen Sie die Registerkarte **Standardeigenschaften** aus.
3.  Wählen Sie im Listenfeld **Standardauthentifizierungsebene** die Option **(Keine)** aus.
4.  Klicken Sie auf die Schaltfläche **OK** .

## <a name="turning-off-call-security-programmatically"></a>Programmgesteuertes Deaktivieren der Anrufsicherheit

Um die Sicherheit programmgesteuert zu deaktivieren, müssen sowohl der Client als auch der Server **CoInitializeSecurity** aufrufen und die Authentifizierungsebene im *dwAuthnLevel-Parameter* auf RPC \_ C \_ AUTHN \_ LEVEL NONE \_ festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deaktivieren der Aktivierungssicherheit](turning-off-activation-security.md)
</dt> </dl>

 

 




