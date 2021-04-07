---
title: Klassen Vererbung im Active Directory Schema
description: Alle Objektklassen in einem Active Directory Directory-Dienst Schema sind von der besonderen Klasse Top abgeleitet.
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038796"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Klassen Vererbung im Active Directory Schema

Alle Objektklassen in einem Active Directory Directory-Dienst Schema sind von der besonderen Klasse [**Top**](/windows/desktop/ADSchema/c-top)abgeleitet. Mit der Ausnahme " **Top**" sind alle Objektklassen Unterklassen einer anderen Objektklasse. [**Contact**](/windows/desktop/ADSchema/c-contact) ist beispielsweise eine Unterklasse von [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson). **OrganizationalPerson** ist eine Unterklasse von [**Person**](/windows/desktop/ADSchema/c-person). und " **Person** " ist eine Unterklasse von " **Top**". Das [**subClassOf**](/windows/desktop/ADSchema/a-subclassof) -Attribut eines [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekts ist eine einwertige Eigenschaft, die die unmittelbare übergeordnete Klasse der Klasse angibt.

Einige der Attributwerte, die eine Klasse definieren, werden von ihren übergeordneten Klassen geerbt. Die [**Contact**](/windows/desktop/ADSchema/c-contact) -Klasse erbt daher Werte von den übergeordneten Klassen, die die Klassen " [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)", " [**Person**](/windows/desktop/ADSchema/c-person)" und " [**Top**](/windows/desktop/ADSchema/c-top) " sind. Eine Klasse erbt die folgenden Daten von den übergeordneten Klassen:

-   Mögliche Attribute: die Werte der Attribute [**mustare**](/windows/desktop/ADSchema/a-mustcontain), [**mayare**](/windows/desktop/ADSchema/a-maycontain), [**systemmustinstance**](/windows/desktop/ADSchema/a-systemmustcontain)und [**systemmaytribute**](/windows/desktop/ADSchema/a-systemmaycontain) eines [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekts definieren eine komplette Liste der Attribute, die für eine Instanz der Objektklasse festgelegt werden können. Für jede Objektklasse enthalten die Werte dieser Attribute alle Werte, die von den übergeordneten Klassen geerbt werden, sowie alle Werte, die explizit für die Objektklasse selbst festgelegt werden. Daher enthält das [**mustattribute**](/windows/desktop/ADSchema/a-mustcontain) -Attribut der [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson) -Klasse alle **mustare** -Werte, die von den Klassen " [**Person**](/windows/desktop/ADSchema/c-person) " und " [**Top**](/windows/desktop/ADSchema/c-top) " geerbt werden, sowie alle **mustare** -Werte, die explizit für die **OrganizationalPerson** -Klasse festgelegt werden.
-   Mögliche übergeordnete Elemente in der Verzeichnishierarchie: die Werte der Attribute " [**posstribute**](/windows/desktop/ADSchema/a-posssuperiors) " und " [**systemposstribute**](/windows/desktop/ADSchema/a-systemposssuperiors) " eines [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekts definieren eine komplette Liste der Objektklassen, die eine Instanz der Objektklasse enthalten können. Für jede Objektklasse enthalten die Werte die Werte, die von den übergeordneten Klassen geerbt werden, sowie diejenigen, die explizit für die Objektklasse selbst festgelegt wurden.

Beachten Sie, dass die Objektklasse auch über viele Erweiterungs Klassen verfügen kann, die in den " [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass) "-und " [**systemAuxiliaryClass**](/windows/desktop/ADSchema/a-systemauxiliaryclass) "-Attributen eines **classSchema** -Objekts angegeben werden. Eine Objektklasse erbt die Werte [**mustare**](/windows/desktop/ADSchema/a-mustcontain), [**mayare**](/windows/desktop/ADSchema/a-maycontain), [**systemmustare**](/windows/desktop/ADSchema/a-systemmustcontain)und [**systemmayare**](/windows/desktop/ADSchema/a-systemmaycontain) aus den zugehörigen Erweiterungs Klassen.

 

 