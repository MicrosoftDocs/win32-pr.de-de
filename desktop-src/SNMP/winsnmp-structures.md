---
title: WinSNMP-Strukturen
description: Die WinSNMP-API-Funktionen verwenden die folgenden Strukturen.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP-Strukturen SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858352"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="43045-104">WinSNMP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="43045-104">WinSNMP Structures</span></span>

<span data-ttu-id="43045-105">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="43045-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="43045-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="43045-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="43045-107">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="43045-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="43045-108">Die WinSNMP-API-Funktionen verwenden die folgenden Strukturen.</span><span class="sxs-lookup"><span data-stu-id="43045-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="43045-109">Struktur</span><span class="sxs-lookup"><span data-stu-id="43045-109">Structure</span></span>                                  | <span data-ttu-id="43045-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43045-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43045-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="43045-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="43045-112">Enthält einen 64-Bit-Ganzzahl-Wert ohne Vorzeichen, der einen Leistungs Bezeichner darstellt.</span><span class="sxs-lookup"><span data-stu-id="43045-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="43045-113">**smioctets**</span><span class="sxs-lookup"><span data-stu-id="43045-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="43045-114">Enthält einen Zeiger auf eine SNMP-Oktett-Zeichenfolge variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="43045-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="43045-115">**smioid**</span><span class="sxs-lookup"><span data-stu-id="43045-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="43045-116">Enthält einen Zeiger auf ein Array variabler Länge der unter Elemente, die einem angegebenen benannten Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="43045-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="43045-117">**smivalue**</span><span class="sxs-lookup"><span data-stu-id="43045-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="43045-118">Stellt den Wert dar, der einem Variablennamen in einem Variablen Bindungs Eintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="43045-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="43045-119">**smivendorinfo**</span><span class="sxs-lookup"><span data-stu-id="43045-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="43045-120">Enthält Informationen über die Microsoft-Implementierung von winsnmp.</span><span class="sxs-lookup"><span data-stu-id="43045-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 