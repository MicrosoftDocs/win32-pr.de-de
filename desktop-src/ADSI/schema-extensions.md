---
title: Schema Erweiterungen
description: Die Architektur des ADSI-Schemas stellt dar, dass dem Schema Klassencontainer neue Schema Klassen und neuen Eigenschaften zur Laufzeit hinzugefügt werden können.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100558"
---
# <a name="schema-extensions"></a><span data-ttu-id="c9536-103">Schema Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="c9536-103">Schema Extensions</span></span>

<span data-ttu-id="c9536-104">Die Architektur des ADSI-Schemas stellt dar, dass dem Schema Klassencontainer neue Schema Klassen und neuen Eigenschaften zur Laufzeit hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="c9536-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="c9536-105">Die zweite Möglichkeit erfordert keinen neuen Code.</span><span class="sxs-lookup"><span data-stu-id="c9536-105">The latter ability requires no new code.</span></span> <span data-ttu-id="c9536-106">Dies ist ein wichtiges Feature für Namespaces, die erweiterbare Verzeichnisdienste ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c9536-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="c9536-107">Die Anbieter Komponente muss diese Erweiterbarkeit zulassen und wissen, wo Sie auf die Klasseninstanz und die Werte ihrer Eigenschaften zugreifen und diese speichern können.</span><span class="sxs-lookup"><span data-stu-id="c9536-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="c9536-108">In einem typischen erweiterbaren Verzeichnisdienst werden diese Informationen in der Verzeichnisdienst Datenbank auf die gleiche Weise gespeichert wie alle anderen Schema Klassen-und Eigenschafts Definitionen.</span><span class="sxs-lookup"><span data-stu-id="c9536-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="c9536-109">In der Terminologie der COM-Schnittstelle können nur Eigenschaften zu einer vorhandenen Schema Klasse und nicht zu Methoden hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c9536-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="c9536-110">Das Hinzufügen einer neuen Methode erfordert das Hinzufügen einer neuen Implementierung dieser Methode und erfordert daher zusätzlichen Code.</span><span class="sxs-lookup"><span data-stu-id="c9536-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="c9536-111">Ein Beispiel für ein bestimmtes Anbieter Schema finden Sie unter [Schema Verwaltung](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="c9536-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




