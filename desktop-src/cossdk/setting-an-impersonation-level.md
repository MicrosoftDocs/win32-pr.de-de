---
description: Wenn Sie eine Identitätswechsel Ebene für eine Anwendung festlegen, legen Sie fest, in welchem Maß an Autorität die Anwendung anderen Anwendungen die Verwendung Ihrer Identität beim Aufrufen erteilt.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Festlegen einer Identitätswechsel Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127013"
---
# <a name="setting-an-impersonation-level"></a>Festlegen einer Identitätswechsel Ebene

Wenn Sie eine Identitätswechsel Ebene für eine Anwendung festlegen, legen Sie fest, in welchem Maß an Autorität die Anwendung anderen Anwendungen die Verwendung Ihrer Identität beim Aufrufen erteilt. Dies kann nur für com+-Server Anwendungen festgelegt werden – Bibliotheksanwendungen werden mit der Identität des Host Prozesses ausgeführt und verwenden die von ihm festgelegte Identitätswechsel Ebene. Weitere Details finden Sie unter Identitätswechsel [Ebenen](/windows/desktop/com/impersonation-levels).

**So wählen Sie eine Identitätswechsel Ebene aus**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie den Identitätswechsel festlegen, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit** .

3.  Wählen Sie im Feld Identitätswechsel **Ebene** die entsprechende Ebene aus. Die folgenden Ebenen sind von der Gewährung der größtmöglichen Autorität abgeleitet:

    -   **Anonym**. Der Client ist gegenüber dem Server anonym. Der Server kann die Identität des Clients annehmen, aber das Identitätswechsel Token (lokale Anmelde Informationen) enthält keine Informationen zum Client.
    -   **Identifizieren** Sie. Der Server kann die Identität des Clients abrufen und die Identität des Clients annehmen, um ACL-Überprüfungen durchzuführen.
    -   Identität **annehmen.** Der Server kann die Identität des Clients annehmen, während er in seinem Namen agiert, obwohl mit Einschränkungen. Der Server kann auf Ressourcen auf dem gleichen Computer wie der Client zugreifen. Wenn sich der Server auf demselben Computer wie der-Client befindet, kann er auf Netzwerkressourcen als Client zugreifen. Wenn sich der-Server auf einem anderen Computer als der-Client befindet, kann er nur auf Ressourcen zugreifen, die sich auf demselben Computer wie der-Server befinden. Dies ist die Standardeinstellung für com+-Server Anwendungen.
    -   **Delegat.** Der Server kann die Identität des Clients annehmen, während er in seinem Namen agiert, egal ob auf dem gleichen Computer wie der Client. Während des Identitäts Wechsels können die Anmelde Informationen des Clients (sowohl mit lokalen als auch mit dem Netzwerk Gültigkeitsdauer) an eine beliebige Anzahl von Computern übermittelt werden.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md)
</dt> <dt>

[Konfigurieren der Software Einschränkungs Richtlinie](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Festlegen einer Authentifizierungs Ebene für eine Server Anwendung](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
