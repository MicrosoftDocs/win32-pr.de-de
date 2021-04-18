---
description: Die setinstalllevel-Methode des Session-Objekts legt die Installations Ebene für die aktuelle Installation auf einen angegebenen Wert fest und berechnet die SELECT-und install-Zustände für alle Features in der Featuretabelle neu.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. setinstalllevel-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354810"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="7a472-103">Session. setinstalllevel-Methode</span><span class="sxs-lookup"><span data-stu-id="7a472-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="7a472-104">Die **setinstalllevel** -Methode des [**Session**](session-object.md) -Objekts legt die Installations Ebene für die aktuelle Installation auf einen angegebenen Wert fest und berechnet die SELECT-und install-Zustände für alle Features in der Featuretabelle neu.</span><span class="sxs-lookup"><span data-stu-id="7a472-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="7a472-105">Außerdem wird der Aktions Status der einzelnen Komponenten in der [Komponenten Tabelle](component-table.md) basierend auf der neuen Ebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7a472-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a472-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a472-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="7a472-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a472-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a472-108">*installLevel*</span><span class="sxs-lookup"><span data-stu-id="7a472-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="7a472-109">Die angeforderte neue Installations Ebene ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a472-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a472-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a472-110">Return value</span></span>

<span data-ttu-id="7a472-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a472-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a472-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a472-112">Remarks</span></span>

<span data-ttu-id="7a472-113">Die [costinitialize-Aktion](costinitialize-action.md) muss vor dem Aufrufen von **setinstalllevel** ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7a472-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="7a472-114">Wenn für den Parameter " *INSTALLLEVEL* " der Wert 0 übergeben wird, wird die aktuelle Installations Ebene nicht geändert, aber alle Funktionen werden nach wie vor auf der aktuellen Installations Ebene aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7a472-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="7a472-115">Diese Funktion kann z. b. vom Handlermodul verwendet werden, um die gesamte Auswahl an einem beliebigen Punkt im Benutzeroberflächen-Auswahl Vorgang auf Ihre anfänglichen Standardzustände zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="7a472-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="7a472-116">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="7a472-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a472-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a472-117">Requirements</span></span>



| <span data-ttu-id="7a472-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a472-118">Requirement</span></span> | <span data-ttu-id="7a472-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7a472-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a472-120">Version</span><span class="sxs-lookup"><span data-stu-id="7a472-120">Version</span></span><br/> | <span data-ttu-id="7a472-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a472-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7a472-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7a472-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7a472-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a472-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7a472-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7a472-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a472-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a472-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7a472-126">IID</span><span class="sxs-lookup"><span data-stu-id="7a472-126">IID</span></span><br/>     | <span data-ttu-id="7a472-127">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7a472-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




