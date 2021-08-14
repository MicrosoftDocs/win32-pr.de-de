---
title: Gewähren von Zugriffsrechten für das Dienstanmeldungskonto
description: Ein Hauptüberlegungen bei der Installation einer Dienstinstanz besteht darin, sicherzustellen, dass der installierte Dienst auf die erforderlichen Ressourcen zugreifen kann.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Gewähren von Zugriffsrechten für das Dienstanmeldungskonto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d13d3e06432b3501961f65a3e27ca00a46f18197bef23d78e6f7ca0deec59b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189079"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Gewähren von Zugriffsrechten für das Dienstanmeldungskonto

Ein Hauptüberlegungen bei der Installation einer Dienstinstanz besteht darin, sicherzustellen, dass der installierte Dienst auf die erforderlichen Ressourcen zugreifen kann. Legen Sie dazu ACEs in den Sicherheitsbeschreibungen von Objekten fest, auf die der Dienst zugreifen muss. Ein ACE kann einem angegebenen Sicherheitsprinzipal Zugriffsrechte gewähren oder verweigern, z. B. dem Dienstbenutzerkonto, dem Computerkonto für einen LocalSystem-Dienst oder einer Gruppe, zu der das Dienstkonto gehört. Weitere Informationen zu ACEs, Sicherheitsbeschreibungen und Zugriffssteuerung finden Sie unter [Steuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) und [Access Control](/windows/desktop/SecAuthZ/access-control).

Weitere Informationen und ein Codebeispiel, mit dem ein ACE festgelegt werden kann, der es dem Dienst ermöglicht, seinen Dienstverbindungspunkt zu ändern, finden Sie unter Enabling Service Account to Access SCP Properties ( Aktivieren des [Dienstkontos für den Zugriff auf SCP-Eigenschaften).](enabling-service-account-to-access-scp-properties.md)

In einigen Fällen müssen Sie Ihr Dienstbenutzerkonto als Mitglied einer oder mehrerer Sicherheitsgruppen hinzufügen. Wenn Sie z. B. eine Administratorengruppe für Ihren Dienst erstellen, können Sie den Dienst zu einem Mitglied der Gruppe machen. Sie können der Gruppe dann Zugriffsrechte gewähren, anstatt sie explizit dem Dienstkonto zu gewähren. Weitere Informationen zu Sicherheitsgruppen finden Sie unter [Verwalten von Gruppen.](managing-groups.md)

 

 