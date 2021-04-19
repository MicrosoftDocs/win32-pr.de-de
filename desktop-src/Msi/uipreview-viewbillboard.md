---
description: Die viewbillboard-Methode des uipreview-Objekts zeigt ein erstelltes Billboard mithilfe des Host Steuer Elements im momentan angezeigten Dialogfeld an.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Uipreview. viewbillboard-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356473"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="294b3-103">Uipreview. viewbillboard-Methode</span><span class="sxs-lookup"><span data-stu-id="294b3-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="294b3-104">Die **viewbillboard** -Methode des [**uipreview**](uipreview-object.md) -Objekts zeigt ein erstelltes Billboard mithilfe des Host Steuer Elements im momentan angezeigten Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="294b3-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="294b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="294b3-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="294b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="294b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="294b3-107">*control*</span><span class="sxs-lookup"><span data-stu-id="294b3-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="294b3-108">Der erforderliche Name des-Steuer Elements, das das Billboard (Unterscheidung nach Groß-/Kleinschreibung) mit dem Dialogfeld und die Primärschlüssel der Steuerungsdaten Bank Tabelle gehostet.</span><span class="sxs-lookup"><span data-stu-id="294b3-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="294b3-109">*Billboard*</span><span class="sxs-lookup"><span data-stu-id="294b3-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="294b3-110">Der erforderliche Name des mit dem angegebenen Steuerelement und dem aktuellen Dialogfeld anzuzeigenden Billboards und der Primärschlüssel der Tabelle mit den Datenbanktabellen.</span><span class="sxs-lookup"><span data-stu-id="294b3-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="294b3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="294b3-111">Return value</span></span>

<span data-ttu-id="294b3-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="294b3-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="294b3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="294b3-113">Requirements</span></span>



| <span data-ttu-id="294b3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="294b3-114">Requirement</span></span> | <span data-ttu-id="294b3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="294b3-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="294b3-116">Version</span><span class="sxs-lookup"><span data-stu-id="294b3-116">Version</span></span><br/> | <span data-ttu-id="294b3-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="294b3-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="294b3-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="294b3-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="294b3-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="294b3-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="294b3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="294b3-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="294b3-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="294b3-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="294b3-122">IID</span><span class="sxs-lookup"><span data-stu-id="294b3-122">IID</span></span><br/>     | <span data-ttu-id="294b3-123">IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="294b3-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




