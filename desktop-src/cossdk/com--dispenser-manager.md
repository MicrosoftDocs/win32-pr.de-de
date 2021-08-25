---
description: Der Verteiler-Manager stellt Ressourcenpooling für die Ressourcenverteiler bereit und stellt sicher, dass eine von einem Ressourcenverteiler bereitgestellte Ressource ordnungsgemäß in die Transaktion der Anwendungsobjekte eingetragen wird.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: COM+-Verteiler-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec090ba8c6324363c80a00685e4bc9cfa11185fa1b95ad5db3575608c9fe60ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991690"
---
# <a name="com-dispenser-manager"></a>COM+-Verteiler-Manager

Der Verteiler-Manager stellt Ressourcenpooling für die Ressourcenverteiler bereit und stellt sicher, dass eine von einem Ressourcenverteiler bereitgestellte Ressource ordnungsgemäß in die Transaktion des Anwendungsobjekts eingetragen wird. Der Verteiler-Manager gibt automatisch Ressourcen frei, die am Ende der Lebensdauer eines Objekts noch reserviert sind, sodass es nicht zu Ressourcenverlusten kommt. Der Verteiler-Manager kann einen Ressourcenverteiler bitten, eine neue Ressource zu erstellen oder Ressourcen im Leerlauf zu zerstören, wenn dies erforderlich ist, um die Lagerbestände anzupassen, anstatt statische Einstellungen zu verwenden.

> [!Note]  
> Da Ressourcenverteilerschnittstellen, die für die Anwendung verfügbar gemacht werden, keine COM-Schnittstellen sein müssen, kann der Verteiler-Manager in einem Prozess verwendet werden, ohne COM zu initialisieren, z. B. um den ODBC-Ressourcenspender zu unterstützen.

 

Bei der Ressourcenerstellung kann der Ressourcenverteiler angeben, wie lange eine Ressource im Leerlauf im Pool verbleiben darf, bevor sie zerstört wird. Ein Thread, der im Verteiler-Manager ausgeführt wird, sucht immer nach diesen Ressourcen im Leerlauf.

## <a name="the-inventory-statistics-manager"></a>Der Bestandsstatistik-Manager

Der Verteiler-Manager verwendet den *Inventurstatistik-Manager* zum Verwalten der Ressourceninventurebenen des Pools. Der Bestandsstatistik-Manager verwaltet einen Datensatz darüber, wann jede Ressource verwendet wurde, und entfernt Ressourcen aus dem Bestand, wenn sie x *Sekunden* lang nicht verwendet wurden, wobei der Wert von *x* pro Ressource festgelegt wird, wenn die Ressource erstellt wird.

## <a name="the-holder-component"></a>Die Halterkomponente

Der Verteiler-Manager fragt alle 10 Sekunden jeden *Besitzer* ab, eine vom Verteiler-Manager erstellte Komponente, die den Ressourcenbestand für jeden Ressourcenverteiler auflistet, um die Neuanpassung des Ressourcenbestands zu ermöglichen. Jeder Besitzer ruft den Bestandsstatistik-Manager auf, um Inventurebenen für jeden Ressourcentyp vorzuschlagen. Daher kann der Besitzer den Ressourcenverteiler bitten, einen Bestand zu erstellen oder zu zerstören.

Der Besitzer und der Ressourcenverteiler kommunizieren, um Ressourcen eines bestimmten Typs anzufordern. Zwischen dem Besitzer und dem Ressourcenspender bestehen die folgenden Beziehungen:

-   Der Besitzer kann eine Ressource vom Ressourcenverteiler anfordern. Der Ressourcenverteiler gibt entweder eine verfügbare Ressource zurück oder erstellt eine neue Ressource.
-   Der Besitzer kann den Ressourcenverteiler benachrichtigen, dass eine Anwendung eine Ressource nicht mehr benötigt, und diese dann an den Ressourcenpool zurückgeben.
-   Der Besitzer und der Ressourcenverteiler arbeiten zusammen, um die Größe des Ressourcenpools beizubehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Ressourcenverteilerkonzepte](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



