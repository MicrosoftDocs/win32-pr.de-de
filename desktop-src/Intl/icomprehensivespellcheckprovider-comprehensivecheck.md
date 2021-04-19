---
description: 'Überprüfen Sie den Anbieter Text auf eine gründlichere Weise als ispellcheckprovider:: Check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Icomprehensivespellcheckprovider:: comprehensivecheck-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350176"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="e8565-103">Icomprehensivespellcheckprovider:: comprehensivecheck-Methode</span><span class="sxs-lookup"><span data-stu-id="e8565-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="e8565-104">Überprüfen Sie den Anbieter Text auf eine gründlichere Weise als [**ispellcheckprovider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="e8565-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8565-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8565-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="e8565-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8565-107">*Text* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8565-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8565-108">Der zu Überprüfung Ende Text.</span><span class="sxs-lookup"><span data-stu-id="e8565-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="e8565-109">*Ergebnis* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e8565-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8565-110">Das Ergebnis der Überprüfung dieses Texts als eine Enumeration von Rechtschreibfehlern ([**ienumspellingerror**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e8565-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8565-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8565-111">Return value</span></span>

<span data-ttu-id="e8565-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e8565-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e8565-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8565-113">Return value</span></span>                                                                             | <span data-ttu-id="e8565-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8565-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e8565-115"><dt>S \_ OK</dt></span><span class="sxs-lookup"><span data-stu-id="e8565-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="e8565-116">Erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e8565-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="e8565-117"><dt>E \_ invalidArg</dt></span><span class="sxs-lookup"><span data-stu-id="e8565-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="e8565-118">*Text* ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e8565-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="e8565-119"><dt>E- \_ Zeiger</dt></span><span class="sxs-lookup"><span data-stu-id="e8565-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="e8565-120">*Text* ist ein NULL-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="e8565-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="e8565-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8565-121">Remarks</span></span>

<span data-ttu-id="e8565-122">Diese Schnittstelle muss nicht von einem Rechtschreib Prüfungs Anbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8565-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="e8565-123">Wenn der Anbieter jedoch zwei "Modi" für die Rechtschreibprüfung unterstützt (eine schnellere und eine langsamere, aber gründlichere), sollte er diese Schnittstelle in demselben Objekt implementieren, das [**ispellcheckprovider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) implementiert, um den gründlicheren Überprüfungs Modus zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e8565-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="e8565-124">Wenn ein Client [**ispellchecker:: comprehensivecheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)aufruft, führt die Rechtschreibprüfungs Funktion den Anbieter für [**icomprehensivespellcheckprovider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider) [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aus und ruft **icomprehensivespellcheckprovider. verständsivecheck** auf, wenn die Schnittstelle unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e8565-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="e8565-125">Wenn die Schnittstelle nicht unterstützt wird, wird Sie automatisch auf [**ispellcheckprovider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)zurückgegriffen.</span><span class="sxs-lookup"><span data-stu-id="e8565-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="e8565-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8565-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8565-127">**Icomprehensivespellcheckprovider**</span><span class="sxs-lookup"><span data-stu-id="e8565-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="e8565-128">**Ienumspellingerror**</span><span class="sxs-lookup"><span data-stu-id="e8565-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="e8565-129">**Ispellchecker:: comprehensivecheck**</span><span class="sxs-lookup"><span data-stu-id="e8565-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="e8565-130">**Ispellcheckprovider**</span><span class="sxs-lookup"><span data-stu-id="e8565-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="e8565-131">**Ispellcheckprovider:: Check**</span><span class="sxs-lookup"><span data-stu-id="e8565-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
