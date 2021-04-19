---
description: Die formattext-Methode des Datensatz-Objekts formatiert Felder gemäß der Vorlage in Feld 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Record. formattext-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369179"
---
# <a name="recordformattext-method"></a><span data-ttu-id="5c46d-103">Record. formattext-Methode</span><span class="sxs-lookup"><span data-stu-id="5c46d-103">Record.FormatText method</span></span>

<span data-ttu-id="5c46d-104">Die **formattext** -Methode des [**Datensatz**](record-object.md) -Objekts formatiert Felder gemäß der Vorlage in Feld 0.</span><span class="sxs-lookup"><span data-stu-id="5c46d-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c46d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c46d-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="5c46d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c46d-106">Parameters</span></span>

<span data-ttu-id="5c46d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5c46d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c46d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c46d-108">Return value</span></span>

<span data-ttu-id="5c46d-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c46d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c46d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c46d-110">Remarks</span></span>

<span data-ttu-id="5c46d-111">Die **formattext** -Methode folgt der Funktion der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion, wenn **msiformatrecord** ein NULL-Installer-Handle als ersten Parameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5c46d-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="5c46d-112">Folglich werden nur die Parameter für das Daten Satz Feld verarbeitet, und die Eigenschaften sind nicht für die Ersetzung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c46d-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="5c46d-113">Beispielsweise wird eine Zeichenfolge, z. b. "Formatieren dieses Felds: \[ 1 \] , Formatieren dieser Eigenschaft: \[ Eigenschaft \] " aufgelöst in "dieses Feld formatieren: Wert aus Feld 1. Formatieren Sie diese Eigenschaft: \[ Eigenschaft \] ."</span><span class="sxs-lookup"><span data-stu-id="5c46d-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="5c46d-114">Parameter, die [formatiert](formatted.md) werden sollen, werden in eckige Klammern eingeschlossen \[ ... \] .</span><span class="sxs-lookup"><span data-stu-id="5c46d-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="5c46d-115">Die eckigen Klammern können iteriert werden, da die Ersetzungen von innen nach oben aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="5c46d-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="5c46d-116">Wenn ein Teil der Zeichenfolge in geschweiften Klammern ({}) eingeschlossen ist und keine eckigen Klammern enthält, bleibt er unverändert, einschließlich der geschweiften Klammern.</span><span class="sxs-lookup"><span data-stu-id="5c46d-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="5c46d-117">Beachten Sie, dass **formattext** im Fall von [benutzerdefinierten Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)nur einen begrenzten Satz von Eigenschaften unterstützt: die Eigenschaften customaktiondata und ProductCode.</span><span class="sxs-lookup"><span data-stu-id="5c46d-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="5c46d-118">Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="5c46d-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c46d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c46d-119">Requirements</span></span>



| <span data-ttu-id="5c46d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c46d-120">Requirement</span></span> | <span data-ttu-id="5c46d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5c46d-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c46d-122">Version</span><span class="sxs-lookup"><span data-stu-id="5c46d-122">Version</span></span><br/> | <span data-ttu-id="5c46d-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c46d-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5c46d-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c46d-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5c46d-125">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c46d-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5c46d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5c46d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c46d-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c46d-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5c46d-128">IID</span><span class="sxs-lookup"><span data-stu-id="5c46d-128">IID</span></span><br/>     | <span data-ttu-id="5c46d-129">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5c46d-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="5c46d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c46d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c46d-131">**Msiformatrecord**</span><span class="sxs-lookup"><span data-stu-id="5c46d-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="5c46d-132">Großformatige</span><span class="sxs-lookup"><span data-stu-id="5c46d-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="5c46d-133">Spaltendatentypen</span><span class="sxs-lookup"><span data-stu-id="5c46d-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




