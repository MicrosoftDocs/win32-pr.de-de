---
description: Anmelde Informationsanbieter in Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Anmelde Informationsanbieter in Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a7947000e5d5a989f71dcdddd808a8e1d5ab3f
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "104350828"
---
# <a name="credential-providers-in-windows-10"></a>Anmelde Informationsanbieter in Windows 10

Anmelde Informationsanbieter sind der primäre Mechanismus für die Benutzerauthentifizierung – Sie sind derzeit die einzige Methode, mit der Benutzer ihre Identität nachweisen können, die für die Anmeldung und andere System Authentifizierungs Szenarien erforderlich ist. Mit Windows 10 und der Einführung von Microsoft Passport sind Anmelde Informationsanbieter wichtiger als je zuvor. Sie werden für die Authentifizierung bei apps, Websites und mehr verwendet.

Microsoft bietet eine Vielzahl von Anmelde Informationsanbietern als Teil von Windows an, z. b. Kennwort, PIN, Smartcard und Windows Hello (Fingerabdruck, Gesichtserkennung und Iris-Erkennung). Diese werden in diesem Artikel als "System Anmelde Informationsanbieter" bezeichnet. OEMs, Unternehmen und andere Entitäten können Ihre eigenen Anmelde Informationsanbieter schreiben und problemlos in Windows integrieren. Diese werden in diesem Artikel als "Anmelde Informationsanbieter von Drittanbietern" bezeichnet. Beachten Sie, dass in Windows 10 sowohl v1-als auch v2-Anmelde Informationsanbieter unterstützt werden. Es ist wichtig, dass Entwickler und Manager von Anmelde Informationsanbietern von Drittanbietern diese Empfehlungen verstehen.

## <a name="system-credential-providers"></a>System Anmelde Informationsanbieter

Es wird dringend empfohlen, dass für jeden Benutzer auf dem Gerät immer mindestens ein System Anmelde Informationsanbieter vorhanden ist, zusätzlich zu allen Anmelde Informationsanbietern von Drittanbietern. Außerdem sollte während der Einrichtung des Drittanbieter-Anmelde Informationsanbieters jeder Benutzer auf dem Gerät aufgefordert werden, mindestens einen System Anmelde Informationsanbieter einzurichten (wenn keine anderen Wiederherstellungsoptionen verfügbar sind, siehe Szenario A, siehe Szenario A).

### <a name="scenario-a"></a>Szenario A

Ein lokaler Kontobenutzer hat einen Drittanbieter für Anmelde Informationen eingerichtet und verwendet ihn regelmäßig zum Anmelden beim Gerät. Ein Tag, an dem der Benutzer ein Update auf dem Gerät installiert, das den Anmelde Informationsanbieter eines Drittanbieters unterbricht, und der Benutzer weiß diese Änderung nicht, bevor der Computer neu gestartet wird.

Beim nächsten Neustart befindet sich der Benutzer auf dem Anmeldebildschirm und kann den erwarteten Drittanbieter-Anmelde Informationsanbieter nicht verwenden. Wenn der Benutzer einen System Anmelde Informationsanbieter eingerichtet hat, kann der Benutzer sich mit diesem beim Computer anmelden. Wenn dies nicht der Fall ist, kann der Benutzer das Konto nicht auf dem Computer wiederherstellen.

### <a name="scenario-b"></a>Szenario B

Ein MSA/AD/Aad-Kontobenutzer hat einen Drittanbieter für Anmelde Informationen eingerichtet und verwendet ihn regelmäßig zum Anmelden beim Gerät. Ein Tag, an dem der Benutzer ein Update auf dem Gerät installiert, das den Anmelde Informationsanbieter eines Drittanbieters unterbricht, und der Benutzer weiß diese Änderung nicht, bevor der Computer neu gestartet wird.

Beim nächsten Neustart befindet sich der Benutzer auf dem Anmeldebildschirm und kann den erwarteten Drittanbieter-Anmelde Informationsanbieter nicht verwenden. Wenn der Benutzer einen System Anmelde Informationsanbieter eingerichtet hat, kann der Benutzer sich mit diesem beim Computer anmelden. Wenn der Anbieter für Kenn Wort Anmelde Informationen des Systems verfügbar ist, kann der Benutzer alternativ das Kennwort per Remote Zugriff anfordern bzw. zurücksetzen und dieses zum Anmelden am Computer verwenden. Wenn keine der Optionen verfügbar ist, kann der Benutzer das Konto nicht auf dem Computer wiederherstellen.

### <a name="conclusion"></a>Zusammenfassung

Zusammenfassend soll verhindert werden, dass alle System Anmelde Informationsanbieter auf einem Gerät deaktiviert werden. Während Anmelde Informationsanbieter von Drittanbietern zusätzliche Authentifizierungsanforderungen für bestimmte Gruppen von Benutzern erfüllen können, ist es sehr wichtig, sicherzustellen, dass der Benutzer bei Auftreten einer Breaking Change immer wieder auf seinen Computer zugreifen kann. System Anmelde Informationsanbieter bieten diese Garantie.

## <a name="custom-credential-providers"></a>Benutzerdefinierte Anmelde Informationsanbieter

Das Windows-Anmelde Informationsanbieter-Framework ermöglicht Entwicklern das Erstellen von benutzerdefinierten Anmelde Informationsanbietern. Wenn [Winlogon](winlogon.md) Anmelde Informationen erfassen möchte, fragt die Anmelde Benutzeroberfläche jeden Anmelde Informationsanbieter nach der Anzahl von Anmelde Informationen ab, die aufgelistet werden sollen. Nachdem alle Anbieter Ihre Kacheln aufgezählt haben, werden Sie von der Anmelde Benutzeroberfläche dem Benutzer angezeigt. Der Benutzer interagiert dann mit einer Kachel, um die erforderlichen Anmelde Informationen bereitzustellen. Die Anmelde Benutzeroberfläche übermittelt diese Anmelde Informationen zur Authentifizierung. Anmelde Informationsanbieter können auch von der Benutzeroberfläche für Anmelde Informationen verwendet werden, wenn Anmelde Informationen erforderlich sind. Eine Liste der Szenarien, in denen ein Anmelde Informationsanbieter unterstützt werden kann, finden Sie unter [**\_ \_ Verwendungs \_ Szenario**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) des Anmelde Informationsanbieters.

Dank dieses Systems ist es viel einfacher, einen Anmelde Informationsanbieter zu erstellen als in der Vergangenheit. Ein Großteil der Arbeit wird durch die Kombination aus [Winlogon](winlogon.md), der Anmelde Benutzeroberfläche und der Benutzeroberfläche für Anmelde Informationen verarbeitet. Zu diesem Zweck müssen Sie eine eigene Implementierung von [**ikredentialprovider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) und [**ikredentialprovidercredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential)erstellen. Wenn Sie einen v2-Anmelde Informationsanbieter implementieren, der empfohlen wird, müssen Sie auch [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2)implementieren.

Beachten Sie, dass es sich bei Anmelde Informationsanbietern nicht um Erzwingungs Mechanismen handelt. Sie werden einfach verwendet, um Anmelde Informationen zu erfassen und zu serialisieren und Sie zur Autorisierung zu übermitteln. Die lokale Autorität und die Authentifizierungs Pakete behandeln und jede erforderliche Sicherheits Durchsetzung.

Kombinieren von Anmelde Informationsanbietern mit unterstützter Hardware können Sie Windows erweitern, um die Anmeldung mit biometrischen Informationen, Kenn Wörtern, Pins, Smartcardzertifikaten oder einem beliebigen benutzerdefinierten Authentifizierungs Paket, das Sie erstellen möchten, zu unterstützen. Sie können die Anmeldung für den Benutzer auf verschiedene Weise anpassen. Wenn die Anmelde Benutzeroberfläche z. b. Ihren Anmelde Informationsanbieter nach den Kacheln der Anmelde Informationen fragt, können Sie eine Standard Kachel angeben, um einen benutzerdefinierten Benutzeroberfläche bereitzustellen. Anmelde Informationsanbieter können sogar für die Unterstützung von einmaligem Anmelden (Single Sign-on, SSO) konzipiert werden, um Benutzer bei einem sicheren Zugriffspunkt und bei der Computer Anmeldung zu authentifizieren.

Anmelde Informationsanbieter werden auf einem Windows-Computer registriert und sind für Folgendes verantwortlich.

-   Beschreiben der Anmelde Informationen, die für die Authentifizierung erforderlich sind.
-   Verarbeiten der Kommunikation und der Logik mit externen Authentifizierungs stellen.
-   Verpacken der Anmelde Informationen für die interaktive und die Netzwerk Anmeldung.

> [!TIP]
>
> Beachten Sie, dass mehrere Anmelde Informationsanbieter auf einem einzelnen Computer installiert werden können.

## <a name="wrapping-credential-providers"></a>Umpacken von Anmelde Informationsanbietern

Das umwickeln eines System Anmelde Informationsanbieters kann durchgeführt werden, um diesem Anmelde Informationsanbieter Funktionen hinzuzufügen, die nicht System intern unterstützt werden. Dies wird nicht empfohlen, da dies zu einem problematischen Verhalten führen kann. An dem Anmelde Informationsanbieter können Änderungen vorgenommen werden, die einen Konflikt mit dem Wrapper verursachen können, was zu einem schlechten Benutzer Verhalten führt oder sogar dazu führt, dass der Benutzer nicht mehr auf sein Gerät gelangt. Dies gilt insbesondere für den häufigen Update Rhythmus von Windows 10.

Wenn Funktionalität in einem Anmelde Informationsanbieter benötigt wird, die nicht System intern enthalten ist, wird der empfohlene Pfad zum Erstellen eines benutzerdefinierten Anmelde Informationsanbieters empfohlen. Dies ist ein stabilerer Ansatz, bei dem keine Abhängigkeiten von den Systemanbietern berücksichtigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vom Anmelde Informationsanbieter gesteuerte Windows-Anmeldevorgang](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[Ikredentialprovider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[Anmelde Informationen für Anmelde Informations \_ Anbieter- \_ \_ Serialisierung](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[\_ \_ Verwendungs Szenario für Anmelde Informationsanbieter \_](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
