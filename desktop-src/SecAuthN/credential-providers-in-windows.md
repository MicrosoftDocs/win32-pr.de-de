---
description: Anmeldeinformationsanbieter in Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Anmeldeinformationsanbieter in Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38543127709007407c013a2a8ff047f7c91f4440351653061e894f4e7c2d90d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008798"
---
# <a name="credential-providers-in-windows-10"></a>Anmeldeinformationsanbieter in Windows 10

Anmeldeinformationsanbieter sind der primäre Mechanismus für die Benutzerauthentifizierung– sie sind derzeit die einzige Methode, mit der Benutzer ihre Identität nachweisen können, die für die Anmeldung und andere Systemauthentifizierungsszenarien erforderlich ist. Mit Windows 10 und der Einführung von Microsoft Passport sind Anmeldeinformationsanbieter wichtiger denn je. Sie werden für die Authentifizierung bei Apps, Websites und mehr verwendet.

Microsoft stellt im Rahmen Windows eine Vielzahl von Anmeldeinformationsanbietern bereit, z. B. Kennwort, PIN, Smartcard und Windows Hello (Fingerabdruck-, Gesichts- und Iriserkennung). Diese werden in diesem Artikel als "Systemanmeldeinformationsanbieter" bezeichnet. OEMs, Unternehmen und andere Entitäten können ihre eigenen Anmeldeinformationsanbieter schreiben und einfach in Windows integrieren. Diese werden in diesem Artikel als "Drittanbieter für Anmeldeinformationen" bezeichnet. Beachten Sie, dass sowohl V1- als auch V2-Anmeldeinformationsanbieter in Windows 10 unterstützt werden. Es ist wichtig, dass Ersteller und Manager von Anmeldeinformationsanbietern von Drittanbietern diese Empfehlungen verstehen.

## <a name="system-credential-providers"></a>Anbieter von Systemanmeldeinformationen

Es wird dringend empfohlen, dass für jeden Benutzer auf dem Gerät immer mindestens ein Anbieter von Systemanmeldeinformationen verfügbar ist, zusätzlich zu allen Anmeldeinformationsanbietern von Drittanbietern. Darüber hinaus sollte während der Einrichtung des Anmeldeinformationsanbieters eines Drittanbieters jeder Benutzer auf dem Gerät aufgefordert werden, mindestens einen Systemanmeldeinformationsanbieter einzurichten (wenn keine anderen Wiederherstellungsoptionen verfügbar sind; siehe Szenario A weiter unten).

### <a name="scenario-a"></a>Szenario A

Ein lokaler Kontobenutzer hat einen Anmeldeinformationsanbieter eines Drittanbieters eingerichtet und verwendet ihn regelmäßig, um sich beim Gerät anzumelden. An einem Tag installiert der Benutzer ein Update auf dem Gerät, das den Anmeldeinformationsanbieter des Drittanbieters unterbricht, und dem Benutzer ist diese Änderung vor dem Neustart des Computers nicht bekannt.

Beim nächsten Neustart befindet sich der Benutzer auf dem Anmeldebildschirm und kann den erwarteten Drittanbieter für Anmeldeinformationen nicht verwenden. Wenn der Benutzer einen Anbieter für Systemanmeldeinformationen eingerichtet hat, kann sich der Benutzer mithilfe dieses Anbieters beim Computer anmelden. Falls nicht, kann der Benutzer das Konto auf dem Computer nicht wiederherstellen.

### <a name="scenario-b"></a>Szenario B

Ein MSA-/AD/AAD-Kontobenutzer hat einen Anmeldeinformationsanbieter eines Drittanbieters eingerichtet und verwendet ihn regelmäßig, um sich beim Gerät anzumelden. An einem Tag installiert der Benutzer ein Update auf dem Gerät, das den Anmeldeinformationsanbieter eines Drittanbieters unterbricht, und dem Benutzer ist diese Änderung vor dem Neustart des Computers nicht bekannt.

Beim nächsten Neustart befindet sich der Benutzer auf dem Anmeldebildschirm und kann den erwarteten Drittanbieter für Anmeldeinformationen nicht verwenden. Wenn der Benutzer einen Anbieter für Systemanmeldeinformationen eingerichtet hat, kann sich der Benutzer mithilfe dieses Anbieters beim Computer anmelden. Wenn der Kennwortanmeldeinformationsanbieter des Systems verfügbar ist, kann der Benutzer alternativ das Kennwort remote anfordern/zurücksetzen und es verwenden, um sich beim Computer anzumelden. Wenn keine der beiden Optionen verfügbar ist, kann der Benutzer das Konto auf dem Computer nicht wiederherstellen.

### <a name="conclusion"></a>Zusammenfassung

Zusammenfassend möchten wir davon abraten, alle Systemanmeldeinformationsanbieter auf einem Gerät zu deaktivieren. Obwohl Anbieter von Anmeldeinformationen von Drittanbietern möglicherweise zusätzliche Authentifizierungsanforderungen für bestimmte Benutzergruppen erfüllen, ist es sehr wichtig sicherzustellen, dass der Benutzer immer wieder Zugriff auf seinen Computer erhalten kann, wenn eine breaking change auftritt. Anbieter von Systemanmeldeinformationen bieten diese Garantie.

## <a name="custom-credential-providers"></a>Benutzerdefinierte Anmeldeinformationsanbieter

Mit dem Windows Framework für Anmeldeinformationsanbieter können Entwickler benutzerdefinierte Anmeldeinformationsanbieter erstellen. Wenn [Winlogon](winlogon.md) Anmeldeinformationen sammeln möchte, fragt die Anmelde-UI jeden Anmeldeinformationsanbieter nach der Anzahl der Anmeldeinformationen ab, die er auflisten möchte. Nachdem alle Anbieter ihre Kacheln aufzählt haben, werden sie dem Benutzer auf der Anmeldeoberfläche angezeigt. Der Benutzer interagiert dann mit einer Kachel, um die erforderlichen Anmeldeinformationen zur Verfügung zu stellen. Die Anmeldeoberfläche übermittelt diese Anmeldeinformationen zur Authentifizierung. Anmeldeinformationsanbieter können auch von der Benutzeroberfläche für Anmeldeinformationen verwendet werden, wenn Anmeldeinformationen erforderlich sind. Eine Liste der Szenarien, in denen ein Anmeldeinformationsanbieter unterstützt werden kann, finden Sie unter [**\_ \_ \_ VERWENDUNGSSZENARIO**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) FÜR ANMELDEINFORMATIONSANBIETER.

Dank dieses Systems ist es viel einfacher, einen Anmeldeinformationsanbieter zu erstellen als in der Vergangenheit. Ein Großteil der Arbeit wird durch die Kombination aus [Winlogon,](winlogon.md)der Anmeldeoberfläche und der Benutzeroberfläche für Anmeldeinformationen erledigt. Hierzu müssen Sie Ihre eigene Implementierung von [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) und [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential)erstellen. Wenn Sie einen V2-Anmeldeinformationsanbieter implementieren, was empfohlen wird, müssen Sie auch [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2)implementieren.

Beachten Sie, dass Anmeldeinformationsanbieter keine Erzwingungsmechanismen sind. Sie werden einfach verwendet, um Anmeldeinformationen zu sammeln und zu serialisieren und zur Autorisierung zu übermitteln. Die lokale Autorität und die Authentifizierungspakete verarbeiten alle erforderlichen Sicherheitserzwingungen.

Durch die Kombination von Anmeldeinformationsanbietern mit unterstützter Hardware können Sie Windows erweitern, um die Anmeldung mit biometrischen Informationen, Kennwörtern, PINs, Smartcardzertifikaten oder einem beliebigen benutzerdefinierten Authentifizierungspaket zu unterstützen, das Sie erstellen möchten. Sie können die Anmeldeerfahrung für den Benutzer auf verschiedene Weise anpassen. Wenn beispielsweise die Anmeldeoberfläche Ihren Anmeldeinformationsanbieter nach den Kacheln für Anmeldeinformationen abfragt, können Sie eine Standardkachel angeben, um eine benutzerdefinierte Benutzeroberfläche für einen Benutzer bereitzustellen. Anmeldeinformationsanbieter können sogar so entworfen werden, dass sie einmaliges Anmelden (Single Sign-On, SSO) unterstützen, Benutzer bei einem sicheren Zugriffspunkt authentifizieren und sich an einem Computer anmelden.

Anmeldeinformationsanbieter werden auf einem Windows Computer registriert und sind für Folgendes verantwortlich.

-   Beschreibung der für die Authentifizierung erforderlichen Anmeldeinformationen.
-   Behandeln der Kommunikation und Logik mit externen Authentifizierungsstellen.
-   Verpacken der Anmeldeinformationen für die interaktive Anmeldung und Netzwerkanmeldung.

> [!TIP]
>
> Beachten Sie, dass mehrere Anmeldeinformationsanbieter auf einem einzelnen Computer installiert werden können.

## <a name="wrapping-credential-providers"></a>Umschließen von Anmeldeinformationsanbietern

Umschließen eines Systemanmeldeinformationsanbieters kann durchgeführt werden, um diesem Anmeldeinformationsanbieter Funktionen hinzuzufügen, die nicht nativ unterstützt werden. Dies wird nicht empfohlen, da dies zu problematischen Verhaltensweisen führen kann. Änderungen können am Anmeldeinformationsanbieter vorgenommen werden, was zu einem Konflikt mit dem Wrapper führen kann, was zu einer schlechten Benutzererfahrung führt oder sogar verhindert, dass der Benutzer auf sein Gerät gelangt. Dies gilt insbesondere für den häufigen Aktualisierungshäufigkeitsgrad von Windows 10.

Wenn Funktionen in einem Anmeldeinformationsanbieter erforderlich sind, die nicht nativ enthalten sind, wird empfohlen, einen benutzerdefinierten Anmeldeinformationsanbieter zu erstellen. Dies ist ein stabilerer Ansatz, der keine Abhängigkeiten von den Systemanbietern übernimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anmeldeinformationsanbieter-gesteuerte Windows-Anmeldung](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[\_ \_ SERIALISIERUNG VON ANMELDEINFORMATIONSINFORMATIONEN DES ANMELDEINFORMATIONSANBIETERS \_](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[\_VERWENDUNGSSZENARIO FÜR ANMELDEINFORMATIONSANBIETER \_ \_](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
