---
description: Die Merge-Methode des Merge-Objekts führt einen Merge der aktuellen Datenbank und des aktuellen Moduls aus.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge. Merge-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365634"
---
# <a name="mergemerge-method"></a><span data-ttu-id="d261b-103">Merge. Merge-Methode</span><span class="sxs-lookup"><span data-stu-id="d261b-103">Merge.Merge method</span></span>

<span data-ttu-id="d261b-104">Die **Merge** -Methode des [**Merge**](merge-object.md) -Objekts führt einen Merge der aktuellen Datenbank und des aktuellen Moduls aus.</span><span class="sxs-lookup"><span data-stu-id="d261b-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="d261b-105">Der Merge fügt die Komponenten im Modul an die Funktion an, die durch die *Funktion* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d261b-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="d261b-106">Der Stamm der Verzeichnisstruktur des Moduls wird an den von *redirectdir* angegebenen Speicherort umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d261b-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="d261b-107">Die **Merge** -Methode kann nur einmal aufgerufen werden, um eine bestimmte Kombination aus MSI-und MSM-Dateien zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="d261b-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="d261b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d261b-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="d261b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d261b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d261b-110">*Feature*</span><span class="sxs-lookup"><span data-stu-id="d261b-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="d261b-111">Der Name einer Funktion in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d261b-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="d261b-112">*Redirectdir*</span><span class="sxs-lookup"><span data-stu-id="d261b-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="d261b-113">Der Schlüssel eines Eintrags in der [Verzeichnis Tabelle](directory-table.md) der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d261b-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="d261b-114">Dieser Parameter kann NULL oder eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="d261b-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d261b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d261b-115">Return value</span></span>

<span data-ttu-id="d261b-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d261b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d261b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d261b-117">Remarks</span></span>

<span data-ttu-id="d261b-118">Nachdem die Zusammenführung fertiggestellt wurde, werden die Komponenten im Modul an das von der *Funktion* identifizierte Feature angefügt.</span><span class="sxs-lookup"><span data-stu-id="d261b-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="d261b-119">Diese Funktion wird nicht erstellt und muss ein vorhandenes Feature sein.</span><span class="sxs-lookup"><span data-stu-id="d261b-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="d261b-120">Beachten Sie, dass die **Merge** -Methode alle Funktions Verweise im Modul abruft und die Funktionsreferenz für alle Vorkommen der NULL-GUID in der Modul Datenbank ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d261b-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="d261b-121">Weitere Informationen finden Sie unter [verweisen auf Features in Mergemodulen](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="d261b-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="d261b-122">Das Modul kann mit der [**Connect**](merge-connect.md) -Methode an zusätzliche Features angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d261b-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="d261b-123">Beachten Sie, dass durch den Aufruf der **Connect** -Methode nur Funktionskomponenten Zuordnungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d261b-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="d261b-124">Die Zeilen, die bereits in der Datenbank zusammengeführt wurden, werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d261b-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="d261b-125">Änderungen, die an der Datenbank vorgenommen werden, werden nur dann gespeichert, wenn die Methode [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) aufgerufen wird und *bcommit* auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d261b-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="d261b-126">Wenn Mergekonflikte auftreten, einschließlich Ausschlüsse, werden Sie für den späteren Abruf in den Fehler Enumerator eingefügt, führen jedoch nicht zu einem Fehler bei der Zusammenführung.</span><span class="sxs-lookup"><span data-stu-id="d261b-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="d261b-127">Fehler können mithilfe der [**Errors**](error-object.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d261b-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="d261b-128">Fehler und Informationsmeldungen werden in der aktuellen Protokolldatei gepostet.</span><span class="sxs-lookup"><span data-stu-id="d261b-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="d261b-129">C++</span><span class="sxs-lookup"><span data-stu-id="d261b-129">C++</span></span>

<span data-ttu-id="d261b-130">Siehe [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d261b-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d261b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d261b-131">Requirements</span></span>



| <span data-ttu-id="d261b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d261b-132">Requirement</span></span> | <span data-ttu-id="d261b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d261b-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d261b-134">Version</span><span class="sxs-lookup"><span data-stu-id="d261b-134">Version</span></span><br/> | <span data-ttu-id="d261b-135">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d261b-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d261b-136">Header</span><span class="sxs-lookup"><span data-stu-id="d261b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d261b-137"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="d261b-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d261b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d261b-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="d261b-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d261b-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
