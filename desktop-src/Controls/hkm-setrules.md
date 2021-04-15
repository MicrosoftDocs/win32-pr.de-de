---
title: HKM_SETRULES Meldung (kommstrg. h)
description: Definiert die ungültigen Kombinationen und die standardmodifiziererkombination für ein Hot Key-Steuerelement.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Windows-Steuerelemente für HKM_SETRULES Meldung
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477295"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="8a3d3-104">HKM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="8a3d3-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="8a3d3-105">Definiert die ungültigen Kombinationen und die standardmodifiziererkombination für ein Hot Key-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a3d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a3d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a3d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a3d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a3d3-108">Ein Array von-Flags, die ungültige Tastenkombinationen angeben.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="8a3d3-109">Dieser Parameter kann eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="8a3d3-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="8a3d3-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8a3d3-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="8a3d3-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a3d3-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="8a3d3-112"><dt>**hkcomb \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="8a3d3-113">ALT</span><span class="sxs-lookup"><span data-stu-id="8a3d3-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="8a3d3-114"><dt>**hkcomb- \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="8a3d3-115">STRG</span><span class="sxs-lookup"><span data-stu-id="8a3d3-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="8a3d3-116"><dt>**hkcomb-Zertifizierungsstelle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="8a3d3-117">STRG + ALT</span><span class="sxs-lookup"><span data-stu-id="8a3d3-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="8a3d3-118"><dt>**hkcomb \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="8a3d3-119">Nicht geänderte Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8a3d3-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="8a3d3-120"><dt>**hkcomb \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="8a3d3-121">Schuss</span><span class="sxs-lookup"><span data-stu-id="8a3d3-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="8a3d3-122"><dt>**hkcomb- \_ sa**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="8a3d3-123">UMSCHALT+ALT</span><span class="sxs-lookup"><span data-stu-id="8a3d3-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="8a3d3-124"><dt>**hkcomb \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="8a3d3-125">UMSCHALT + STRG</span><span class="sxs-lookup"><span data-stu-id="8a3d3-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="8a3d3-126"><dt>**hkcomb \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="8a3d3-127">UMSCHALT + STRG + ALT</span><span class="sxs-lookup"><span data-stu-id="8a3d3-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="8a3d3-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a3d3-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a3d3-129">Ein Array von Flags, die die Tastenkombination angeben, die verwendet werden soll, wenn der Benutzer eine ungültige Kombination eingibt.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="8a3d3-130">Eine Liste der modifiziererflagwerte finden Sie in der Beschreibung der [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a3d3-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a3d3-131">Return value</span></span>

<span data-ttu-id="8a3d3-132">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3d3-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a3d3-133">Remarks</span></span>

<span data-ttu-id="8a3d3-134">Wenn ein Benutzer eine ungültige Tastenkombination eingibt, die durch in *wParam* angegebene Flags definiert ist, verwendet das System den bitweisen OR-Operator, um die vom Benutzer eingegebenen Schlüssel mit den in *LPARAM* angegebenen Flags zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="8a3d3-135">Die resultierende Tastenkombination wird in eine Zeichenfolge konvertiert und dann im Steuerelement "Hot Key" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a3d3-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3d3-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a3d3-136">Requirements</span></span>



| <span data-ttu-id="8a3d3-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a3d3-137">Requirement</span></span> | <span data-ttu-id="8a3d3-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8a3d3-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3d3-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a3d3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8a3d3-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a3d3-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a3d3-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a3d3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8a3d3-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a3d3-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a3d3-143">Header</span><span class="sxs-lookup"><span data-stu-id="8a3d3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a3d3-144"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a3d3-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





