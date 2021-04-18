---
description: Bei der TargetPath-Eigenschaft des Sitzungs Objekts handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die den vollständigen Pfad zum angegebenen Ordner auf dem Installationsziel Laufwerk bereitstellt.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Session. TargetPath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364467"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="5d800-103">Session. TargetPath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5d800-103">Session.TargetPath property</span></span>

<span data-ttu-id="5d800-104">Bei der **TargetPath** -Eigenschaft des [**Sitzungs**](session-object.md) Objekts handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die den vollständigen Pfad zum angegebenen Ordner auf dem Installationsziel Laufwerk bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5d800-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="5d800-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5d800-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d800-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d800-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5d800-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5d800-107">Property value</span></span>

<span data-ttu-id="5d800-108">Unter Berücksichtigung der Groß-/Kleinschreibung für eine Ordner Eigenschaft, die durch einen Primärschlüssel der [Verzeichnis Tabelle](directory-table.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d800-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="5d800-109">Wenn der Ordner nicht vorhanden ist, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="5d800-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d800-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d800-110">Remarks</span></span>

<span data-ttu-id="5d800-111">Versuchen Sie nicht, den Zielpfad zu konfigurieren, wenn die Komponenten, die diese Pfade verwenden, für den aktuellen Benutzer oder für einen anderen Benutzer bereits installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5d800-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="5d800-112">Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) , um zu bestimmen, ob das Produkt, das die Komponente enthält, installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5d800-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="5d800-113">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="5d800-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d800-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d800-114">Requirements</span></span>



| <span data-ttu-id="5d800-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d800-115">Requirement</span></span> | <span data-ttu-id="5d800-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5d800-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d800-117">Version</span><span class="sxs-lookup"><span data-stu-id="5d800-117">Version</span></span><br/> | <span data-ttu-id="5d800-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d800-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d800-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d800-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d800-120">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d800-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5d800-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5d800-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d800-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d800-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5d800-123">IID</span><span class="sxs-lookup"><span data-stu-id="5d800-123">IID</span></span><br/>     | <span data-ttu-id="5d800-124">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d800-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




