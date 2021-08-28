---
description: In COM+ wird der freigegebene vorübergehende Zustand für Objekte mithilfe des freigegebenen Eigenschaften-Managers (Shared Property Manager, SPM) verwaltet. Der SPM ist ein Ressourcenverteiler, mit dem Sie den Zustand für mehrere Objekte innerhalb eines Serverprozesses freigeben können.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: COM+-Konzepte für freigegebene Eigenschaften-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9ce190cb4f4e65e6ab5208dd2adec08f807d4f6d29d4cf99a3e70a1c0a7004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129012"
---
# <a name="com-shared-property-manager-concepts"></a>COM+-Konzepte für freigegebene Eigenschaften-Manager

In COM+ wird der freigegebene vorübergehende Zustand für Objekte mithilfe des freigegebenen Eigenschaften-Managers (Shared Property Manager, SPM) verwaltet. Der SPM ist ein Ressourcenverteiler, mit dem Sie den Zustand für mehrere Objekte innerhalb eines Serverprozesses freigeben können.

Globale Variablen können in einer verteilten Umgebung aufgrund von Parallelitäts- und Namenskonfliktproblemen nicht verwendet werden. Der Freigegebene Eigenschaften-Manager beseitigt Namenskonflikte, indem er freigegebene Eigenschaftengruppen bereitstellt, die eindeutige Namespaces für die freigegebenen Eigenschaften einrichten, die sie enthalten. Der SPM implementiert auch Sperren und Semaphoren, um freigegebene Eigenschaften vor gleichzeitigem Zugriff zu schützen, was zu verlorenen Updates führen und Eigenschaften in einem unvorhersehbaren Zustand belassen kann.

> [!Note]  
> Freigegebener vorübergehender Zustand sind Zustandsinformationen, die im Arbeitsspeicher gespeichert werden und systemfehler nicht überstehen. Die Informationen sind so konzipiert, dass sie von mehreren Objekten über Transaktionsgrenzen hinweg (aber nicht prozessübergreifend) gemeinsam genutzt werden.

 

Freigegebene Eigenschaften, die im SPM gespeichert sind, sind nur für Objekte verfügbar, die im gleichen Prozess ausgeführt werden. Dies bedeutet, dass die Objekte, die das SPM zum Speichern von Werten verwenden und Zugriff auf diese Werte benötigen, als Teil derselben COM+-Anwendung installiert werden müssen. Systemadministratoren können COM+-Klassen von einem Paket in ein anderes verschieben, nachdem Ihre COM+-Anwendung bereitgestellt wurde. Wenn Sie sich auf mehrere Objekte verlassen, die Eigenschaften über das SPM gemeinsam nutzen, sollten Sie eindeutig dokumentieren, dass sie in derselben COM+-Anwendung installiert werden müssen.

Es ist auch wichtig, dass Komponenten, die Eigenschaften gemeinsam nutzen, das gleiche Aktivierungsattribut aufweisen. Wenn zwei Komponenten im selben Paket unterschiedliche Aktivierungsattribute aufweisen, können sie im Allgemeinen keine Eigenschaften gemeinsam nutzen. Wenn beispielsweise eine Komponente für die Ausführung in einem Clientprozess und die andere für die Ausführung in einem Serverprozess konfiguriert ist, werden ihre Objekte in der Regel in verschiedenen Prozessen ausgeführt, obwohl sie sich im selben Paket befinden.

Sie sollten die [**SharedPropertyGroupManager-,**](sharedpropertygroupmanager.md) [**SharedPropertyGroup-**](sharedpropertygroup.md)und [**SharedProperty-Objekte**](sharedproperty.md) immer von COM+-Komponenten statt von einem Basisclient instanziieren. Wenn ein Basisclient freigegebene Eigenschaftengruppen und Eigenschaften erstellt, befinden sich die freigegebenen Eigenschaften im Basisclientprozess und nicht in einem Serverprozess. Dies bedeutet, dass die COM+-Objekte die Eigenschaften nicht gemeinsam nutzen können, es sei denn, die Objekte werden auch im Clientprozess ausgeführt (was im Allgemeinen keine gute Idee ist).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[FREIGEGEBENE COM+-Eigenschaften-Manager](com--shared-property-manager.md)
</dt> <dt>

[Freigegebene Eigenschaftengruppen](shared-property-groups.md)
</dt> </dl>

 

 



