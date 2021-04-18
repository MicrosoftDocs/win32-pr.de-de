---
description: Die mergeex-Methode des Merge-Objekts entspricht der Merge-Funktion, mit der Ausnahme, dass Sie ein zusätzliches Argument annimmt.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Merge. mergeex-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358320"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="8c03b-103">Merge. mergeex-Methode</span><span class="sxs-lookup"><span data-stu-id="8c03b-103">Merge.MergeEx method</span></span>

<span data-ttu-id="8c03b-104">Die **mergeex** -Methode des [**Merge**](merge-object.md) -Objekts entspricht der [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) -Funktion, mit der Ausnahme, dass Sie ein zusätzliches Argument annimmt.</span><span class="sxs-lookup"><span data-stu-id="8c03b-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="8c03b-105">Das *pconfiguration* -Argument ist eine vom Client implementierte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8c03b-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="8c03b-106">Das Argument kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8c03b-106">The argument may be null.</span></span> <span data-ttu-id="8c03b-107">Das vorhanden sein dieses Arguments gibt an, dass der Client die Konfigurationsfunktionen unterstützen kann, aber den Client nicht zum Bereitstellen von Konfigurationsdaten für ein bestimmtes konfigurierbares Element löscht.</span><span class="sxs-lookup"><span data-stu-id="8c03b-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="8c03b-108">Die [**Merge**](merge-merge.md) -Methode führt einen Merge der aktuellen Datenbank und des aktuellen Moduls aus.</span><span class="sxs-lookup"><span data-stu-id="8c03b-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="8c03b-109">Der Merge fügt die Komponenten im Modul an die Funktion an, die durch die *Funktion* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8c03b-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="8c03b-110">Der Stamm der Verzeichnisstruktur des Moduls wird an den von *redirectdir* angegebenen Speicherort umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8c03b-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c03b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c03b-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="8c03b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c03b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c03b-113">*Feature*</span><span class="sxs-lookup"><span data-stu-id="8c03b-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="8c03b-114">Der Name einer Funktion in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8c03b-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="8c03b-115">*Redirectdir*</span><span class="sxs-lookup"><span data-stu-id="8c03b-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="8c03b-116">Der Schlüssel eines Eintrags in der [Verzeichnis Tabelle](directory-table.md) der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8c03b-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="8c03b-117">Dieser Parameter kann NULL oder eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="8c03b-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="8c03b-118">*pconfiguration*</span><span class="sxs-lookup"><span data-stu-id="8c03b-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="8c03b-119">Das *pconfiguration* -Argument ist eine vom Client implementierte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8c03b-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="8c03b-120">Das Argument kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8c03b-120">The argument may be null.</span></span> <span data-ttu-id="8c03b-121">Das vorhanden sein dieses Arguments gibt an, dass der Client die Konfigurationsfunktionen unterstützen kann, aber den Client nicht zum Bereitstellen von Konfigurationsdaten für ein bestimmtes konfigurierbares Element löscht.</span><span class="sxs-lookup"><span data-stu-id="8c03b-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c03b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c03b-122">Return value</span></span>

<span data-ttu-id="8c03b-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8c03b-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c03b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c03b-124">Remarks</span></span>

<span data-ttu-id="8c03b-125">Nachdem die Zusammenführung fertiggestellt wurde, werden die Komponenten im Modul an das von der *Funktion* identifizierte Feature angefügt.</span><span class="sxs-lookup"><span data-stu-id="8c03b-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="8c03b-126">Diese Funktion wird nicht erstellt und muss ein vorhandenes Feature sein.</span><span class="sxs-lookup"><span data-stu-id="8c03b-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="8c03b-127">Das Modul kann mit der [**Connect**](merge-connect.md) -Methode an zusätzliche Features angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8c03b-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="8c03b-128">Änderungen, die an der Datenbank vorgenommen werden, werden nur dann gespeichert, wenn die Methode [**CloseDatabase**](merge-closedatabase.md) aufgerufen wird und *bcommit* auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8c03b-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="8c03b-129">Wenn Mergekonflikte auftreten, einschließlich Ausschlüsse, werden Sie für den späteren Abruf in den Fehler Enumerator eingefügt, führen jedoch nicht zu einem Fehler bei der Zusammenführung.</span><span class="sxs-lookup"><span data-stu-id="8c03b-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="8c03b-130">Fehler können mithilfe der [**Errors**](merge-errors.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8c03b-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="8c03b-131">Fehler und Informationsmeldungen werden in der aktuellen Protokolldatei gepostet.</span><span class="sxs-lookup"><span data-stu-id="8c03b-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="8c03b-132">Wenn die Zusammenführung aufgrund einer falschen Modulkonfiguration fehlschlägt, gibt die [**mergeex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) -Funktion E \_ Fail zurück.</span><span class="sxs-lookup"><span data-stu-id="8c03b-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="8c03b-133">Dies schließt folgende msmerrortype-Fehler ein: **msmerrorbadnullsubstitution**, **msmerrorbadsubstitutiontype**, **msmerrorbadnullresponse**, **msmerrormissingconfigitem** und **msmerrordatarequestfailed**.</span><span class="sxs-lookup"><span data-stu-id="8c03b-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="8c03b-134">Diese Fehler bewirken, dass die Zusammenführung sofort beendet wird, wenn der Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8c03b-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="8c03b-135">Das Error-Objekt wird immer noch dem Enumerator hinzugefügt, wenn **mergeex** E Fail zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="8c03b-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="8c03b-136">Weitere Informationen zu msmerrortype-Fehlern finden [**Sie unter Get \_ Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span><span class="sxs-lookup"><span data-stu-id="8c03b-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="8c03b-137">Alle anderen Fehler bewirken, dass **mergeex** den Wert "false" zurückgibt \_ und den Vorgang fortsetzen kann.</span><span class="sxs-lookup"><span data-stu-id="8c03b-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="8c03b-138">C++</span><span class="sxs-lookup"><span data-stu-id="8c03b-138">C++</span></span>

<span data-ttu-id="8c03b-139">Siehe [**mergeex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8c03b-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c03b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c03b-140">Requirements</span></span>



| <span data-ttu-id="8c03b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c03b-141">Requirement</span></span> | <span data-ttu-id="8c03b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="8c03b-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c03b-143">Version</span><span class="sxs-lookup"><span data-stu-id="8c03b-143">Version</span></span><br/> | <span data-ttu-id="8c03b-144">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8c03b-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="8c03b-145">Header</span><span class="sxs-lookup"><span data-stu-id="8c03b-145">Header</span></span><br/>  | <dl> <span data-ttu-id="8c03b-146"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c03b-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c03b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8c03b-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c03b-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c03b-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
