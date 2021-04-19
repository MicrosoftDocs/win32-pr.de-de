---
description: Die setgprm-Methode legt den angegebenen allgemeinen Parameter Register auf den angegebenen Wert fest.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Setgprm-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346811"
---
# <a name="setgprm-method"></a><span data-ttu-id="5df9b-103">Setgprm-Methode</span><span class="sxs-lookup"><span data-stu-id="5df9b-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="5df9b-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5df9b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5df9b-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5df9b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5df9b-106">Die- `SetGPRM` Methode legt den angegebenen allgemeinen Parameter Register auf den angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="5df9b-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="5df9b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df9b-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="5df9b-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="5df9b-109">Gibt das allgemeine Parameter Register an, das als ganze Zahl festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5df9b-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="5df9b-110">Der ganzzahlige Wert muss zwischen 0 und 15 liegen.</span><span class="sxs-lookup"><span data-stu-id="5df9b-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="5df9b-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nWert*</span><span class="sxs-lookup"><span data-stu-id="5df9b-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="5df9b-112">Gibt den neuen Wert für das Register als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="5df9b-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5df9b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5df9b-113">Remarks</span></span>

<span data-ttu-id="5df9b-114">Allgemeine Parameter Register (oder gprms) sind 16-Bit-Register, die von den einzelnen Datenträgern für die temporäre Datenspeicherung auf besondere Weise verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5df9b-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="5df9b-115">Eine Player Anwendung muss nicht auf diese Register für eine Standard Wiedergabe oder ein Navigations Steuerelement mithilfe des **mswebdvd** -Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5df9b-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="5df9b-116">Diese Methode wird für Player Anwendungen bereitgestellt, die erweiterte Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="5df9b-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="5df9b-117">Versuchen Sie nicht, die gprms direkt zu ändern, es sei denn, Sie haben umfassende Kenntnisse über die DVD-Spezifikation und die Art und Weise, in der die gprms auf der zu Wiedergabe enden Festplatte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5df9b-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="5df9b-118">Wenn Sie diese Werte ändern, kann dies zu unvorhersehbarem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="5df9b-118">Changing these values can result in unpredictable behavior.</span></span>

 

 



