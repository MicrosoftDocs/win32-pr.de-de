---
title: Arbeiten mit Variablen Bindungs Listen
description: Eine Variablen Bindung ist die Kopplung eines SNMP-objektinstanznamens mit einem zugeordneten Wert. Eine Variablen Bindungs Liste ist eine Reihe von Variablen Bindungs Einträgen. In WinSNMP enthält eine Protokolldaten Einheit (PDU) eine Variablen Bindungs Liste.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Arbeiten mit Variablen Bindungs Listen SNMP
- Variablen Bindung listet SNMP, SNMP auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723664"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="a317d-107">Arbeiten mit Variablen Bindungs Listen</span><span class="sxs-lookup"><span data-stu-id="a317d-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="a317d-108">Eine *Variablen Bindung* ist die Kopplung eines SNMP-objektinstanznamens mit einem zugeordneten Wert.</span><span class="sxs-lookup"><span data-stu-id="a317d-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="a317d-109">Eine *Variablen Bindungs Liste* ist eine Reihe von Variablen Bindungs Einträgen.</span><span class="sxs-lookup"><span data-stu-id="a317d-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="a317d-110">In WinSNMP enthält eine Protokolldaten Einheit (PDU) eine Variablen Bindungs Liste.</span><span class="sxs-lookup"><span data-stu-id="a317d-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="a317d-111">Die Details der Variablen Bindungs Listenstruktur sind auf die Microsoft WinSNMP-Implementierung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a317d-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="a317d-112">Eine WinSNMP-Anwendung kann auf eine Variablen Bindungs Liste mit einem Handle des Typs **hsnmp \_ VBL** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a317d-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="a317d-113">Weitere Informationen finden Sie unter [Ressourcenhandle-Objekte](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a317d-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="a317d-114">Die WinSNMP-Anwendung kann Variablen Bindungs Listen erstellen und bearbeiten und Sie in PDUs einschließen.</span><span class="sxs-lookup"><span data-stu-id="a317d-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="a317d-115">Zum Ausführen dieser Vorgänge verwendet die Anwendung die WinSNMP- [Variablen Bindungsfunktionen](winsnmp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a317d-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="a317d-116">Weitere Informationen zum Arbeiten mit WinSNMP und Variablen Bindungs Listen finden Sie in den in der folgenden Tabelle aufgeführten Themen.</span><span class="sxs-lookup"><span data-stu-id="a317d-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="a317d-117">Thema</span><span class="sxs-lookup"><span data-stu-id="a317d-117">Topic</span></span>                                                                    | <span data-ttu-id="a317d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a317d-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="a317d-119">Erstellen einer Variablen Bindungs Liste</span><span class="sxs-lookup"><span data-stu-id="a317d-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="a317d-120">Beschreibt, wie eine Variablen Bindungs Liste erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a317d-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="a317d-121">Verwalten einer Variablen Bindungs Liste</span><span class="sxs-lookup"><span data-stu-id="a317d-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="a317d-122">Beschreibt, wie eine Variablen Bindungs Liste verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="a317d-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="a317d-123">Weitere Informationen zu Variablen Bindungen und Variablen Bindungs Listen finden Sie unter [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protokoll Vorgänge für Version 2 des Simple Network Management-Protokolls (SNMPv2)" und der WinSNMP- [Variablen Bindungsfunktionen](winsnmp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a317d-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




