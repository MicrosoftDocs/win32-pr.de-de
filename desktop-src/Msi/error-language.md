---
description: Die schreibgeschützte Language-Eigenschaft des Error-Objekts gibt die langid des aktuellen Fehlers zurück.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Error. Language-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368614"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="05487-103">Error. Language (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05487-103">Error.Language property</span></span>

<span data-ttu-id="05487-104">Die schreibgeschützte **Language** -Eigenschaft des [**Error**](error-object.md) -Objekts gibt die **LangID** des aktuellen Fehlers zurück.</span><span class="sxs-lookup"><span data-stu-id="05487-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="05487-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="05487-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05487-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="05487-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="05487-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="05487-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="05487-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05487-108">Remarks</span></span>

<span data-ttu-id="05487-109">Der Wert der **Language** -Eigenschaft ist-1, es sei denn, der Fehler ist vom Typ msmerrorlanguageunsupported oder msmerrorlanguagefailed.</span><span class="sxs-lookup"><span data-stu-id="05487-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="05487-110">Sie können den Fehlertyp ermitteln, indem Sie die [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05487-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="05487-111">C++</span><span class="sxs-lookup"><span data-stu-id="05487-111">C++</span></span>

<span data-ttu-id="05487-112">Weitere Informationen finden [**Sie unter Get \_ Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span><span class="sxs-lookup"><span data-stu-id="05487-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="05487-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05487-113">Requirements</span></span>



| <span data-ttu-id="05487-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05487-114">Requirement</span></span> | <span data-ttu-id="05487-115">Wert</span><span class="sxs-lookup"><span data-stu-id="05487-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05487-116">Version</span><span class="sxs-lookup"><span data-stu-id="05487-116">Version</span></span><br/> | <span data-ttu-id="05487-117">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="05487-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="05487-118">Header</span><span class="sxs-lookup"><span data-stu-id="05487-118">Header</span></span><br/>  | <dl> <span data-ttu-id="05487-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="05487-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="05487-120">DLL</span><span class="sxs-lookup"><span data-stu-id="05487-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="05487-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05487-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

