---
title: D1103-Handle mit Verlust
ms.assetid: 9bb08cd6-104a-4168-b14e-3caec1679388
description: Eine Schnittstelle wurde erstellt, aber nicht freigegeben.
keywords:
- D1103-handle Direct2D
topic_type:
- apiref
api_name:
- D1103 Leaked Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cc4b4e43f94bd4ceb5d7a2518879c69bd3ecf8f3
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106370893"
---
# <a name="d1103-leaked-handle"></a><span data-ttu-id="13a0f-104">D1103: Handle mit Verlust</span><span class="sxs-lookup"><span data-stu-id="13a0f-104">D1103: Leaked Handle</span></span>

<span data-ttu-id="13a0f-105">Es wurde eine Schnittstellen \[ *Schnittstelle* \] erstellt, aber nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="13a0f-105">An interface \[*interface*\] was created but not released.</span></span>

## <a name="placeholders"></a><span data-ttu-id="13a0f-106">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="13a0f-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="13a0f-107"><span id="interface"></span><span id="INTERFACE"></span>*berfläche*</span><span class="sxs-lookup"><span data-stu-id="13a0f-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="13a0f-108">Die Adresse der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="13a0f-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="13a0f-109">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="13a0f-109">Possible Causes</span></span>

<span data-ttu-id="13a0f-110">Ungültige Ressourcenverwendung.</span><span class="sxs-lookup"><span data-stu-id="13a0f-110">Invalid resource usage.</span></span> <span data-ttu-id="13a0f-111">Eine Anwendung kann eine Schnittstelle nicht freigeben, wenn Sie nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13a0f-111">An application fails to release an interface when it is no longer in use.</span></span>

 

 




