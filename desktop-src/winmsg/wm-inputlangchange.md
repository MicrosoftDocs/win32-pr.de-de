---
description: Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabesprache einer Anwendung geändert wurde. Sie sollten anwendungsspezifische Einstellungen vornehmen und die Nachricht an die DefWindowProc-Funktion übergeben, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332405"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="be926-104">WM \_ INPUTLANGCHANGE-Nachricht</span><span class="sxs-lookup"><span data-stu-id="be926-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="be926-105">Wird an das oberste betroffene Fenster gesendet, nachdem die Eingabesprache einer Anwendung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="be926-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="be926-106">Sie sollten anwendungsspezifische Einstellungen vornehmen und die Nachricht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, die die Nachricht an alle untergeordneten Fenster der ersten Ebene übergibt.</span><span class="sxs-lookup"><span data-stu-id="be926-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="be926-107">Diese untergeordneten Fenster können die Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben, damit die Nachricht an ihre untergeordneten Fenster übergeben wird usw.</span><span class="sxs-lookup"><span data-stu-id="be926-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="be926-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be926-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a><span data-ttu-id="be926-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="be926-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be926-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be926-110">*wParam*</span></span>

</dt> <dd>
  
<span data-ttu-id="be926-111">Typ: **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="be926-111">Type: **WPARAM**</span></span>

<span data-ttu-id="be926-112">Die [Codepage](../Intl/code-pages.md) des neuen Gebietsschemas.</span><span class="sxs-lookup"><span data-stu-id="be926-112">The [code page](../Intl/code-pages.md) of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="be926-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be926-113">*lParam*</span></span>

</dt> <dd>
 
<span data-ttu-id="be926-114">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="be926-114">Type: **LPARAM**</span></span>

<span data-ttu-id="be926-115">Der  HKL-Eingabe-Gebietsschemabezeichner.</span><span class="sxs-lookup"><span data-stu-id="be926-115">The **HKL** input locale identifier.</span></span> <span data-ttu-id="be926-116">Weitere Informationen finden Sie unter [Sprachen, Gebietsschemas und Tastaturlayouts.](../inputdev/about-keyboard-input.md)</span><span class="sxs-lookup"><span data-stu-id="be926-116">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be926-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be926-117">Return value</span></span>

<span data-ttu-id="be926-118">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="be926-118">Type: **LRESULT**</span></span>

<span data-ttu-id="be926-119">Eine Anwendung sollte einen Wert ungleich 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="be926-119">An application should return nonzero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="be926-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="be926-120">Remarks</span></span>

<span data-ttu-id="be926-121">Sie können den [Namen des Tastaturschemas](../Intl/locale-names.md) über [die LCIDToLocaleName-Funktion](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) abrufen.</span><span class="sxs-lookup"><span data-stu-id="be926-121">You can retrieve keyboard [locale name](../Intl/locale-names.md) via [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) function.</span></span> <span data-ttu-id="be926-122">Mit dem Gebietsschemanamen können Sie [moderne Gebietsschemafunktionen](/windows/win32/intl/calling-the--locale-name--functions)verwenden:</span><span class="sxs-lookup"><span data-stu-id="be926-122">With locale name you can use [modern locale functions](/windows/win32/intl/calling-the--locale-name--functions):</span></span>

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a><span data-ttu-id="be926-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be926-123">Requirements</span></span>

| <span data-ttu-id="be926-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be926-124">Requirement</span></span> | <span data-ttu-id="be926-125">Wert</span><span class="sxs-lookup"><span data-stu-id="be926-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be926-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be926-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be926-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be926-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be926-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be926-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be926-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be926-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be926-130">Header</span><span class="sxs-lookup"><span data-stu-id="be926-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="be926-131"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="be926-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="be926-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be926-132">See also</span></span>

<span data-ttu-id="be926-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="be926-133">**Reference**</span></span>

- [<span data-ttu-id="be926-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="be926-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [<span data-ttu-id="be926-135">**WM \_ INPUTLANGCHANGEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="be926-135">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)

<span data-ttu-id="be926-136">**Konzept**</span><span class="sxs-lookup"><span data-stu-id="be926-136">**Conceptual**</span></span>

- [<span data-ttu-id="be926-137">Windows</span><span class="sxs-lookup"><span data-stu-id="be926-137">Windows</span></span>](windows.md) 
