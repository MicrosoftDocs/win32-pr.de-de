---
description: Bestimmt, ob in den Optionen markierte Komponenten auf dem System installiert sind.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Icsgneedinetcomponents-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362038"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="8a569-103">Icsgneedinetcomponents-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a569-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="8a569-104">Bestimmt, ob in den Optionen markierte Komponenten auf dem System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="8a569-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a569-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a569-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="8a569-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a569-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a569-107">*DWF Options*</span><span class="sxs-lookup"><span data-stu-id="8a569-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="8a569-108">Eine Kombination der folgenden Flags, die angeben, welche Komponenten in der folgenden Liste erkannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a569-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="8a569-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8a569-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="8a569-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a569-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="8a569-111"><dt>**ICFG \_ Installmail**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8a569-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="8a569-112">Ist Exchange oder Internet-e-Mail erforderlich?</span><span class="sxs-lookup"><span data-stu-id="8a569-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="8a569-113"><dt>**ICFG \_ Installras**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8a569-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="8a569-114">Ist RAS erforderlich?</span><span class="sxs-lookup"><span data-stu-id="8a569-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="8a569-115"><dt>**ICFG \_ Installtcp**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8a569-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="8a569-116">Ist TCP/IP erforderlich?</span><span class="sxs-lookup"><span data-stu-id="8a569-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="8a569-117">*lpfneedcomponents*</span><span class="sxs-lookup"><span data-stu-id="8a569-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="8a569-118">Wenn dieser Wert nicht **null** ist, ist es bei der Rückgabe **true** , wenn mindestens eine Komponente nicht auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8a569-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a569-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a569-119">Return value</span></span>

<span data-ttu-id="8a569-120">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a569-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8a569-121">Wenn keine Fehler auftreten, wird der **Fehler \_ Erfolgs** Code zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a569-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a569-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a569-122">Remarks</span></span>

<span data-ttu-id="8a569-123">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8a569-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a569-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a569-124">Requirements</span></span>



| <span data-ttu-id="8a569-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a569-125">Requirement</span></span> | <span data-ttu-id="8a569-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8a569-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a569-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8a569-127">DLL</span></span><br/> | <dl> <span data-ttu-id="8a569-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a569-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
