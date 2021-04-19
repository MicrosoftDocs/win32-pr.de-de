---
description: Die OpenModule-Methode des Merge-Objekts öffnet ein Windows Installer Mergemodul im schreibgeschützten Modus. Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge. OpenModule-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372521"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="ac954-104">Merge. OpenModule-Methode</span><span class="sxs-lookup"><span data-stu-id="ac954-104">Merge.OpenModule method</span></span>

<span data-ttu-id="ac954-105">Die **OpenModule** -Methode des [**Merge**](merge-object.md) -Objekts öffnet ein Windows Installer Mergemodul im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="ac954-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="ac954-106">Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac954-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac954-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac954-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="ac954-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac954-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac954-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ac954-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="ac954-110">Voll qualifizierter Dateiname, der auf ein Mergemodul verweist.</span><span class="sxs-lookup"><span data-stu-id="ac954-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="ac954-111">*Sprache*</span><span class="sxs-lookup"><span data-stu-id="ac954-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="ac954-112">Ein gültiger sprach Bezeichner (langid).</span><span class="sxs-lookup"><span data-stu-id="ac954-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac954-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac954-113">Return value</span></span>

<span data-ttu-id="ac954-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac954-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac954-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac954-115">Remarks</span></span>

<span data-ttu-id="ac954-116">Diese Funktion öffnet das Mergemodul im schreibgeschützten Modus und schließt andere Programme vom Schreiben in das Mergemodul aus, bis die [**closemodule**](merge-closemodule.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ac954-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="ac954-117">Das Installationsprogramm versucht, das Modul in der Sprache zu öffnen, die in der *Sprache* angegeben ist, oder eine allgemeinere Sprache.</span><span class="sxs-lookup"><span data-stu-id="ac954-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="ac954-118">Wenn *Language* beispielsweise als 1033 angegeben wird, kann ein Modul mit der Standardsprache 1033, 9 oder 0 in der Standardsprache geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ac954-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="ac954-119">Der *sprach* Wert 9 öffnet Module mit der Standardsprache 9 oder 0.</span><span class="sxs-lookup"><span data-stu-id="ac954-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="ac954-120">Wenn die Standardsprache des Moduls nicht den angegebenen Anforderungen entspricht, wird versucht, das Modul in die angeforderte Sprache umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="ac954-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="ac954-121">Wenn dies nicht möglich ist, wird das Modul in immer mehr allgemeine Sprachen transformiert, und zwar bis zu sprachneutral.</span><span class="sxs-lookup"><span data-stu-id="ac954-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="ac954-122">Wenn keine der Transformationen erfolgreich ist, kann das Modul nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ac954-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="ac954-123">In diesem Fall wird der Fehlerliste des Typs msmerrorlanguageunsupported ein Fehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ac954-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="ac954-124">Wenn beim Transformieren des Moduls in die gewünschte Sprache ein Fehler auftritt, wird der Fehlerliste des Typs msmerrorlanguagefailed ein Fehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ac954-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="ac954-125">Weitere Informationen finden Sie unter der [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ac954-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="ac954-126">Durch das Öffnen eines Mergemoduls werden alle Fehler gelöscht, die noch nicht abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ac954-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="ac954-127">C++</span><span class="sxs-lookup"><span data-stu-id="ac954-127">C++</span></span>

<span data-ttu-id="ac954-128">Siehe [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ac954-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac954-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac954-129">Requirements</span></span>



| <span data-ttu-id="ac954-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac954-130">Requirement</span></span> | <span data-ttu-id="ac954-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ac954-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac954-132">Version</span><span class="sxs-lookup"><span data-stu-id="ac954-132">Version</span></span><br/> | <span data-ttu-id="ac954-133">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ac954-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="ac954-134">Header</span><span class="sxs-lookup"><span data-stu-id="ac954-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ac954-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac954-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac954-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ac954-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac954-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac954-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
