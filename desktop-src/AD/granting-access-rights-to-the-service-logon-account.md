---
title: Erteilen von Zugriffsrechten für das Dienst Anmelde Konto
description: Ein primärer Aspekt beim Installieren einer Dienst Instanz besteht darin sicherzustellen, dass der installierte Dienst auf die erforderlichen Ressourcen zugreifen kann.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Erteilen von Zugriffsrechten für das Dienst Anmelde Konto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106338450"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Erteilen von Zugriffsrechten für das Dienst Anmelde Konto

Ein primärer Aspekt beim Installieren einer Dienst Instanz besteht darin sicherzustellen, dass der installierte Dienst auf die erforderlichen Ressourcen zugreifen kann. Legen Sie hierzu in den Sicherheits Beschreibungen von Objekten, auf die der Dienst zugreifen muss, ACEs fest. Ein ACE kann Zugriffsrechte für einen angegebenen Sicherheits Prinzipal gewähren oder verweigern, wie z. b. das Dienst Benutzerkonto oder das Computer Konto für einen LocalSystem-Dienst oder eine Gruppe, zu der das Dienst Konto gehört. Weitere Informationen zu ACEs, Sicherheits Deskriptoren und Zugriffs Steuerung finden [Sie Untersteuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) und [Access Control](/windows/desktop/SecAuthZ/access-control).

Weitere Informationen und ein Codebeispiel, mit dem ein ACE festgelegt werden kann, der dem Dienst das Ändern des Dienst Verbindungs Punkts ermöglicht, finden Sie unter [Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften](enabling-service-account-to-access-scp-properties.md).

In einigen Fällen müssen Sie Ihr Dienst Benutzerkonto als Mitglied einer oder mehrerer Sicherheitsgruppen hinzufügen. Wenn Sie z. b. eine Gruppe "Administratoren" für den Dienst erstellen, können Sie den Dienst als Mitglied der Gruppe festlegen. Sie können der Gruppe dann Zugriffsrechte erteilen, anstatt Sie explizit dem Dienst Konto zuzuweisen. Weitere Informationen zu Sicherheitsgruppen finden Sie unter [Verwalten von Gruppen](managing-groups.md).

 

 