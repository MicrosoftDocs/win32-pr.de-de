---
description: In com+ wird der freigegebene vorübergehende Zustand für-Objekte mithilfe des freigegebenen Eigenschaften-Managers (SPM) verwaltet. Der SPM ist ein Ressourcen Verteiler, den Sie verwenden können, um den Status von mehreren Objekten innerhalb eines Server Prozesses gemeinsam zu nutzen.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Gemeinsam genutzte com+-Eigenschaften-Manager Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343189"
---
# <a name="com-shared-property-manager-concepts"></a>Gemeinsam genutzte com+-Eigenschaften-Manager Konzepte

In com+ wird der freigegebene vorübergehende Zustand für-Objekte mithilfe des freigegebenen Eigenschaften-Managers (SPM) verwaltet. Der SPM ist ein Ressourcen Verteiler, den Sie verwenden können, um den Status von mehreren Objekten innerhalb eines Server Prozesses gemeinsam zu nutzen.

Globale Variablen können nicht in einer verteilten Umgebung verwendet werden, da Probleme mit Parallelität und Namenskollisionen auftreten. Der freigegebene Eigenschaften-Manager entfernt Namenskonflikte durch Bereitstellen von freigegebenen Eigenschaften Gruppen, die eindeutige Namespaces für die freigegebenen Eigenschaften einrichten, die Sie enthalten. Der SPM implementiert auch sperren und Semaphoren, um freigegebene Eigenschaften vor gleichzeitigem Zugriff zu schützen. Dies kann zu einem Verlust von Updates führen und die Eigenschaften in einem unvorhersehbaren Zustand hinterlassen.

> [!Note]  
> Ein frei gegebener vorübergehender Zustand ist Zustandsinformationen, die im Arbeitsspeicher beibehalten werden und Systemfehler nicht überstehen. Die Informationen sind so konzipiert, dass Sie von mehreren-Objekten über transaktionsübergreifende (aber nicht prozessübergreifende) Grenzen hinweg verwendet werden.

 

Freigegebene Eigenschaften, die im SPM gespeichert sind, sind nur für Objekte verfügbar, die im selben Prozess ausgeführt werden. Dies bedeutet, dass die Objekte, die den SPM zum Speichern von Werten verwenden und auf diese Werte zugreifen müssen, als Teil der gleichen com+-Anwendung installiert werden müssen. Es ist möglich, dass Systemadministratoren com+-Klassen nach der Bereitstellung der com+-Anwendung von einem Paket in ein anderes verschieben. Wenn Sie von mehreren Objekten abhängen, die Eigenschaften über das SPM freigeben, sollten Sie klar dokumentieren, dass Sie in der gleichen com+-Anwendung installiert werden müssen.

Es ist auch wichtig, dass Komponenten, die Eigenschaften gemeinsam nutzen, über das gleiche Aktivierungs Attribut verfügen. Wenn zwei Komponenten im gleichen Paket über unterschiedliche Aktivierungs Attribute verfügen, können diese Eigenschaften in der Regel nicht gemeinsam genutzt werden. Wenn z. b. eine Komponente so konfiguriert ist, dass Sie in einem Client Prozess ausgeführt wird und die andere für die Durchführung in einem Server Prozess konfiguriert ist, werden die Objekte in der Regel in unterschiedlichen Prozessen ausgeführt, auch wenn Sie sich im gleichen Paket befinden.

Sie sollten immer die Objekte [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)und [**SharedProperty**](sharedproperty.md) von COM+-Komponenten anstelle eines Basis Clients instanziieren. Wenn ein Basis Client freigegebene Eigenschaften Gruppen und Eigenschaften erstellt, befinden sich die freigegebenen Eigenschaften innerhalb des Basis Client Prozesses und nicht in einem Server Prozess. Dies bedeutet, dass die COM+-Objekte die Eigenschaften nicht gemeinsam nutzen können, es sei denn, die Objekte werden ebenfalls im Client Prozess ausgeführt (was in der Regel keine gute Idee ist).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gemeinsam genutztes com+-Eigenschaften-Manager](com--shared-property-manager.md)
</dt> <dt>

[Freigegebene Eigenschaften Gruppen](shared-property-groups.md)
</dt> </dl>

 

 



