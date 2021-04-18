---
description: Die viewdialog-Methode des uipreview-Objekts zeigt ein in der aktuellen Datenbank gespeichertes Dialogfeld "Benutzeroberfläche" an.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: Uipreview. viewdialog-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364638"
---
# <a name="uipreviewviewdialog-method"></a><span data-ttu-id="d64a4-103">Uipreview. viewdialog-Methode</span><span class="sxs-lookup"><span data-stu-id="d64a4-103">UIPreview.ViewDialog method</span></span>

<span data-ttu-id="d64a4-104">Die **viewdialog** -Methode des [**uipreview**](uipreview-object.md) -Objekts zeigt ein in der aktuellen Datenbank gespeichertes Dialogfeld "Benutzeroberfläche" an.</span><span class="sxs-lookup"><span data-stu-id="d64a4-104">The **ViewDialog** method of the [**UIPreview**](uipreview-object.md) object displays an authored user interface dialog box stored in the current database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d64a4-105">Syntax</span></span>


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a><span data-ttu-id="d64a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d64a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64a4-107">*Dialog*</span><span class="sxs-lookup"><span data-stu-id="d64a4-107">*dialog*</span></span> 
</dt> <dd>

<span data-ttu-id="d64a4-108">Der erforderliche Name des Dialog Felds, Unterscheidung nach Groß-/Kleinschreibung und der Primärschlüssel der Dialogfeld Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="d64a4-108">Required name of the dialog box, case-sensitive, and the primary key of the Dialog database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64a4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d64a4-109">Return value</span></span>

<span data-ttu-id="d64a4-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d64a4-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d64a4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d64a4-111">Requirements</span></span>



| <span data-ttu-id="d64a4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d64a4-112">Requirement</span></span> | <span data-ttu-id="d64a4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d64a4-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d64a4-114">Version</span><span class="sxs-lookup"><span data-stu-id="d64a4-114">Version</span></span><br/> | <span data-ttu-id="d64a4-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d64a4-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d64a4-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d64a4-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d64a4-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="d64a4-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d64a4-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d64a4-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d64a4-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d64a4-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d64a4-120">IID</span><span class="sxs-lookup"><span data-stu-id="d64a4-120">IID</span></span><br/>     | <span data-ttu-id="d64a4-121">IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d64a4-121">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




