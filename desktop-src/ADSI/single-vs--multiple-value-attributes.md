---
title: Einzelne Attribute und Attribute mit mehreren Werten
description: Die Attribute, die in einem Verzeichnis vorhanden sein können, werden in der Regel im Schema für das Verzeichnis definiert.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- Einzel-und mehrfach Wert Attribute ADSI
- Attribute ADSI, Single-und Multiple Value-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036299"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="deca0-105">Einzelne Attribute und Attribute mit mehreren Werten</span><span class="sxs-lookup"><span data-stu-id="deca0-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="deca0-106">Die Attribute, die in einem Verzeichnis vorhanden sein können, werden in der Regel im Schema für das Verzeichnis definiert.</span><span class="sxs-lookup"><span data-stu-id="deca0-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="deca0-107">Die Schema Definition eines Attributs gibt eine Reihe von Merkmalen des Attributs an, z. b. den Datentyp und ob eine Instanz des Attributs mehrere Werte aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="deca0-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="deca0-108">Eine Instanz eines einwertigen Attributs kann einen einzelnen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="deca0-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="deca0-109">Eine Instanz eines mehrwertigen Attributs kann entweder einen einzelnen Wert oder mehrere Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="deca0-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="deca0-110">Active Directory erstellt keine Attribute mit leeren Werten – entweder enthält das Attribut einen gültigen Wert oder ist im Objekt nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="deca0-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="deca0-111">In Active Directory und den meisten anderen LDAP-Servern ist die Reihenfolge der Werte in einem mehrwertigen Attribut nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="deca0-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="deca0-112">Außerdem muss jeder Wert eines mehrwertigen Attributs eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="deca0-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="deca0-113">ADSI lädt in der Regel Schema Daten, wenn Ihr Verzeichnis ein Schema unterstützt, wie Active Directory.</span><span class="sxs-lookup"><span data-stu-id="deca0-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="deca0-114">Da ADSI die Syntax von Attributen im Schema kennt, ist es nicht erforderlich, den Attributtyp anzugeben, wenn darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="deca0-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="deca0-115">ADSI Marshalls Attributwerte in den entsprechenden Datentyp, wie im Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="deca0-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="deca0-116">Wenn Ihr Verzeichnis kein Schema aufweist, geben Sie den Datentyp an, wenn Sie auf ein Attribut zugreifen.</span><span class="sxs-lookup"><span data-stu-id="deca0-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="deca0-117">Active Directory, Exchange, Windows NT 4,0 und der Standort Server verfügen alle über ein Schema.</span><span class="sxs-lookup"><span data-stu-id="deca0-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="deca0-118">Außerdem verfügt Active Directory über ein erweiterbares Schema.</span><span class="sxs-lookup"><span data-stu-id="deca0-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




