---
title: Imstscadvancedsettings keyboardlayoutstr-Eigenschaft
description: Gibt den Namen des aktiven Eingabe Gebiets Schema Bezeichners (früher als Tastaturlayout bezeichnet) für die Verbindung an.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Keyboardlayoutstr-Eigenschaft Remotedesktopdienste
- Keyboardlayoutstr-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, keyboardlayoutstr-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741504"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="fffa3-106">Imstscadvancedsettings:: keyboardlayoutstr-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fffa3-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="fffa3-107">Gibt den Namen des aktiven Eingabe Gebiets Schema Bezeichners (früher als Tastaturlayout bezeichnet) für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="fffa3-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="fffa3-108">Wenn diese Eigenschaft nicht festgelegt ist, verwendet das Steuerelement das Standardlayout, das von der [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fffa3-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="fffa3-109">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="fffa3-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffa3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fffa3-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="fffa3-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fffa3-111">Property value</span></span>

<span data-ttu-id="fffa3-112">Der Name des aktiven Eingabe Gebiets Schema Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="fffa3-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fffa3-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fffa3-113">Error codes</span></span>

<span data-ttu-id="fffa3-114">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fffa3-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffa3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fffa3-115">Remarks</span></span>

<span data-ttu-id="fffa3-116">Die-Eigenschaft ist eine hexadezimale Zahl mit acht Ziffern in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fffa3-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="fffa3-117">Die unteren vier Ziffern stellen den sprach Bezeichner dar, und die oberen vier Ziffern stellen die Tastatur Variation innerhalb dieser Sprache dar.</span><span class="sxs-lookup"><span data-stu-id="fffa3-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="fffa3-118">Beispielsweise würde "00000409" die Standardtastatur von US-Englisch darstellen, da "0409" der US-englische sprach Bezeichner ist.</span><span class="sxs-lookup"><span data-stu-id="fffa3-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="fffa3-119">Die Dvorak-Variation der US-englischen Tastatur hat den Bezeichner "00010409".</span><span class="sxs-lookup"><span data-stu-id="fffa3-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="fffa3-120">Sie finden die verfügbaren Tastaturlayouts, die nach Ihren Tastaturlayout-bezeichlern aufgeführt sind, in der Registrierung unter</span><span class="sxs-lookup"><span data-stu-id="fffa3-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="fffa3-121">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fffa3-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fffa3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fffa3-122">Requirements</span></span>



| <span data-ttu-id="fffa3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fffa3-123">Requirement</span></span> | <span data-ttu-id="fffa3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fffa3-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffa3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fffa3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fffa3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fffa3-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="fffa3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fffa3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fffa3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fffa3-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fffa3-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fffa3-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="fffa3-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fffa3-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="fffa3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fffa3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffa3-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fffa3-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="fffa3-133">IID</span><span class="sxs-lookup"><span data-stu-id="fffa3-133">IID</span></span><br/>                      | <span data-ttu-id="fffa3-134">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="fffa3-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fffa3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fffa3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffa3-136">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="fffa3-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

