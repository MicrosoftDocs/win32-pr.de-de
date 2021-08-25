---
description: Wenn Sie eine Identitätswechselebene für eine Anwendung festlegen, bestimmen Sie, welchen Autoritätsgrad die Anwendung anderen Anwendungen gewährt, um ihre Identität zu verwenden, wenn sie sie aufruft.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Festlegen einer Identitätswechselebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c23b8d0b54f12cbce92af43187681922854519c69e8614e952fda241e4fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895950"
---
# <a name="setting-an-impersonation-level"></a>Festlegen einer Identitätswechselebene

Wenn Sie eine Identitätswechselebene für eine Anwendung festlegen, bestimmen Sie, welchen Autoritätsgrad die Anwendung anderen Anwendungen gewährt, um ihre Identität zu verwenden, wenn sie sie aufruft. Sie können dies nur für COM+-Serveranwendungen festlegen– Bibliotheksanwendungen werden unter der Identität des Hostingprozesses ausgeführt und verwenden die Identitätswechselebene, die angegeben wird. Weitere Informationen finden Sie unter [Identitätswechselebenen.](/windows/desktop/com/impersonation-levels)

**So wählen Sie eine Identitätswechselebene aus**

1.  Klicken Sie mit der rechten Maustaste auf die COM+-Anwendung, für die Sie den Identitätswechsel festlegen, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Anwendungseigenschaften auf die Registerkarte **Sicherheit.**

3.  Wählen Sie im Feld **Identitätswechselebene** die entsprechende Ebene aus. Die Ebenen sind wie folgt sortiert von der Gewährung der geringsten bis zur größten Autorität:

    -   **Anonym**. Der Client ist gegenüber dem Server anonym. Der Server kann die Identität des Clients annehmen, aber das Identitätswechseltoken (lokale Anmeldeinformationen) enthält keine Informationen zum Client.
    -   **Identifizieren Sie**. Der Server kann die Identität des Clients abrufen und die Identität des Clients annehmen, um ACL-Überprüfungen durchzuführen.
    -   **Annehmen der Identität** von . Der Server kann die Identität des Clients annehmen, während er in seinem Namen handelt, jedoch mit Einschränkungen. Der Server kann auf demselben Computer wie der Client auf Ressourcen zugreifen. Wenn sich der Server auf demselben Computer wie der Client befindet, kann er auf Netzwerkressourcen als Client zugreifen. Wenn sich der Server auf einem anderen Computer als dem Client befindet, kann er nur auf Ressourcen zugreifen, die sich auf demselben Computer wie der Server befinden. Dies ist die Standardeinstellung für COM+-Serveranwendungen.
    -   **Delegieren Sie**. Der Server kann die Identität des Clients annehmen, während er in seinem Namen handelt, unabhängig davon, ob er sich auf demselben Computer wie der Client befindet. Während des Identitätswechsels können die Anmeldeinformationen des Clients (sowohl die anmeldeinformationen mit lokaler als auch diejenigen mit Netzwerkgültigkeit) an eine beliebige Anzahl von Computern übergeben werden.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Role-Based Security](configuring-role-based-security.md)
</dt> <dt>

[Konfigurieren der Softwareeinschränkungsrichtlinie](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Aktivieren der Authentifizierung für eine Bibliotheksanwendung](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Festlegen einer Authentifizierungsebene für eine Serveranwendung](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
