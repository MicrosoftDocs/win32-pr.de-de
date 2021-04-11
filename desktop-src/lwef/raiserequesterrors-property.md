---
title: Raiserequesterrors (Eigenschaft)
description: Raiserequesterrors (Eigenschaft)
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104209188"
---
# <a name="raiserequesterrors-property"></a><span data-ttu-id="bf6b4-103">Raiserequesterrors (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf6b4-103">RaiseRequestErrors Property</span></span>

<span data-ttu-id="bf6b4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bf6b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bf6b4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bf6b4-106">Gibt zurück oder legt fest, ob Fehler für Anforderungen ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-106">Returns or sets whether errors for requests are raised.</span></span>

</dd> <dt>

<span data-ttu-id="bf6b4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bf6b4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bf6b4-108">\*Agent \* \* *. Raiserequesterrors* \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="bf6b4-108">*agent\*\*\*.RaiseRequestErrors*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="bf6b4-109">Teil</span><span class="sxs-lookup"><span data-stu-id="bf6b4-109">Part</span></span>      | <span data-ttu-id="bf6b4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf6b4-110">Description</span></span>                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6b4-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="bf6b4-111">*boolean*</span></span> | <span data-ttu-id="bf6b4-112">Ein boolescher Wert, der bestimmt, ob Fehler in Anforderungen ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-112">A Boolean value that determines whether errors in requests are raised.</span></span><br/> <span data-ttu-id="bf6b4-113">**True**    (Standard) Anforderungs Fehler werden ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-113">**True**    (Default) Request errors are raised.</span></span> <br/> <span data-ttu-id="bf6b4-114">**False**     Anforderungs Fehler werden nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-114">**False**     Request errors are not raised.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf6b4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf6b4-115">Remarks</span></span>

<span data-ttu-id="bf6b4-116">Mit dieser Eigenschaft können Sie feststellen, ob der Server Fehler auslöst, die mit Methoden auftreten, die [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-116">This property enables you to determine whether the server raises errors that occur with methods that support [**Request**](/windows/desktop/lwef/the-request-object) objects.</span></span> <span data-ttu-id="bf6b4-117">Wenn Sie z. b. einen Animations Namen angeben, der nicht in einer [**Wiedergabe**](play-method.md)Methode vorhanden ist, löst der Server einen Fehler aus (der die Fehlermeldung anzeigt), es sei denn, Sie legen diese Eigenschaft auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-117">For example, if you specify an animation name that does not exist in a [**Play**](play-method.md)method, the server raises an error (displaying the error message) unless you set this property to **False**.</span></span>

<span data-ttu-id="bf6b4-118">Dies kann für Programmiersprachen nützlich sein, die keine Wiederherstellung bereitstellen, wenn ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-118">It may be useful for programming languages that do not provide recovery when an error is raised.</span></span> <span data-ttu-id="bf6b4-119">Achten Sie jedoch darauf, dass Sie diese Eigenschaft auf **false** festlegen, da es möglicherweise schwieriger ist, Fehler im Code zu finden.</span><span class="sxs-lookup"><span data-stu-id="bf6b4-119">However, use care when setting this property to **False**, because it might be harder to find errors in your code.</span></span>

 

