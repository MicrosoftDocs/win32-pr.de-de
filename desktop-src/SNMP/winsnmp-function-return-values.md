---
title: Rückgabewerte der WinSNMP-Funktion
description: Der Rückgabewert eines WinSNMP-Funktions Aufrufes kann ein Handle für eine Ressource sein, die von der Microsoft WinSNMP-Implementierung für die WinSNMP-Anwendung zugewiesen wird.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039484"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="c7193-103">Rückgabewerte der WinSNMP-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7193-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="c7193-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c7193-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7193-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c7193-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c7193-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="c7193-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="c7193-107">Der Rückgabewert eines WinSNMP-Funktions Aufrufes kann ein Handle für eine Ressource sein, die von der Microsoft WinSNMP-Implementierung für die WinSNMP-Anwendung zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c7193-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="c7193-108">In der folgenden Tabelle werden die fünf Typen von Ressourcen Handles aufgelistet, die von der-Implementierung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c7193-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="c7193-109">Handle-Typ</span><span class="sxs-lookup"><span data-stu-id="c7193-109">Handle type</span></span>    | <span data-ttu-id="c7193-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7193-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="c7193-111">hsnmp- \_ Sitzung</span><span class="sxs-lookup"><span data-stu-id="c7193-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="c7193-112">Handle für eine WinSNMP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="c7193-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="c7193-113">hsnmp- \_ Entität</span><span class="sxs-lookup"><span data-stu-id="c7193-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="c7193-114">Handle für eine SNMP-Entität</span><span class="sxs-lookup"><span data-stu-id="c7193-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="c7193-115">hsnmp- \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="c7193-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="c7193-116">Handle für einen SNMP-Kontext</span><span class="sxs-lookup"><span data-stu-id="c7193-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="c7193-117">hsnmp- \_ PDU</span><span class="sxs-lookup"><span data-stu-id="c7193-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="c7193-118">Handle für eine Protokolldaten Einheit</span><span class="sxs-lookup"><span data-stu-id="c7193-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="c7193-119">hsnmp- \_ VBL</span><span class="sxs-lookup"><span data-stu-id="c7193-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="c7193-120">Handle für eine Variablen Bindungs Liste</span><span class="sxs-lookup"><span data-stu-id="c7193-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="c7193-121">Weitere Informationen finden Sie unter [Ressourcenhandle-Objekte](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c7193-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="c7193-122">Der Rückgabewert kann auch ein Ganzzahl ohne Vorzeichen Long Integer-Wert des **smiUINT32** -Typs sein, der einen Snmpapi- \_ Status Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7193-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="c7193-123">In der folgenden Tabelle sind die WinSNMP-Statuswerte und ihre Bedeutung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7193-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="c7193-124">Status</span><span class="sxs-lookup"><span data-stu-id="c7193-124">Status</span></span>           | <span data-ttu-id="c7193-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7193-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c7193-126">Snmpapi- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="c7193-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="c7193-127">Gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="c7193-127">Indicates an error.</span></span> <span data-ttu-id="c7193-128">Entspricht 0 oder **null**.</span><span class="sxs-lookup"><span data-stu-id="c7193-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="c7193-129">Snmpapi- \_ Erfolg</span><span class="sxs-lookup"><span data-stu-id="c7193-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="c7193-130">Gibt an, dass die Funktion erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c7193-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="c7193-131">Entspricht 1 oder einer positiven Anzahl.</span><span class="sxs-lookup"><span data-stu-id="c7193-131">Equates to 1 or a positive count.</span></span> |



 

 

 