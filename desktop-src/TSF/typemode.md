---
title: Typemode-Enumeration (Software-BDC. h)
description: Elemente der typemode-Enumeration werden verwendet, um typmodi anzugeben, die für eine weiche Tastatur verfügbar sind.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Typemode-Enumeration Text Services-Framework
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340315"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="6df62-104">Typemode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="6df62-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="6df62-105">Elemente der **typemode** -Enumeration werden verwendet, um typmodi anzugeben, die für eine weiche Tastatur verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6df62-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df62-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6df62-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="6df62-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6df62-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6df62-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**Clickmouse**</span><span class="sxs-lookup"><span data-stu-id="6df62-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="6df62-109">Der Benutzer kann auf die Bildschirmtasten klicken, um Text einzugeben.</span><span class="sxs-lookup"><span data-stu-id="6df62-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="6df62-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hocker**</span><span class="sxs-lookup"><span data-stu-id="6df62-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="6df62-111">Der Benutzer kann für einen vordefinierten Zeitraum auf einen Schlüssel zeigen, und das ausgewählte Zeichen wird automatisch eingegeben.</span><span class="sxs-lookup"><span data-stu-id="6df62-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="6df62-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**DAT**</span><span class="sxs-lookup"><span data-stu-id="6df62-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="6df62-113">Die weiche Tastatur scannt den Eingabebereich ständig und hebt Regionen hervor, in denen der Benutzer eine Tastenkombination drücken oder ein Switch-Input-Gerät verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6df62-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6df62-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6df62-114">Requirements</span></span>



| <span data-ttu-id="6df62-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6df62-115">Requirement</span></span> | <span data-ttu-id="6df62-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6df62-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6df62-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6df62-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6df62-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6df62-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6df62-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6df62-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6df62-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6df62-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6df62-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6df62-121">Redistributable</span></span><br/>          | <span data-ttu-id="6df62-122">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6df62-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="6df62-123">Header</span><span class="sxs-lookup"><span data-stu-id="6df62-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df62-124"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df62-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="6df62-125">IDL</span><span class="sxs-lookup"><span data-stu-id="6df62-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6df62-126"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6df62-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





