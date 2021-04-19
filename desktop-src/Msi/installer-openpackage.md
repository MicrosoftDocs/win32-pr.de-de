---
description: Mit der OpenPackage-Methode des Installer-Objekts wird ein Installer-Paket für die Verwendung mit Funktionen geöffnet, die auf die Produktdatenbank und die Installations-Engine zugreifen und ein Sitzungs Objekt zurückgeben.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer. OpenPackage-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350775"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="4850e-103">Installer. OpenPackage-Methode</span><span class="sxs-lookup"><span data-stu-id="4850e-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="4850e-104">Mit der **OpenPackage** -Methode des [**Installer**](installer-object.md) -Objekts wird ein Installer-Paket für die Verwendung mit Funktionen geöffnet, die auf die Produktdatenbank und die Installations-Engine zugreifen und ein [**Sitzungs**](session-object.md) Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4850e-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4850e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4850e-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="4850e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4850e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4850e-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="4850e-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="4850e-108">Erforderliche Zeichenfolge, die den Pfadnamen des Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="4850e-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="4850e-109">*options*</span><span class="sxs-lookup"><span data-stu-id="4850e-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="4850e-110">Ein optionaler ganzzahliger Wert, der angibt, ob **OpenPackage** beim Erstellen des Sitzungs Objekts den aktuellen Computer Zustand ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="4850e-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="4850e-111">Kein Wert oder der Wert 0 für Optionen ist standardmäßig auf das ursprüngliche Verhalten eingestellt.</span><span class="sxs-lookup"><span data-stu-id="4850e-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="4850e-112">Wenn die Option 1 ist, ignoriert die **OpenPackage** -Methode den aktuellen Computer Status beim Öffnen des Pakets.</span><span class="sxs-lookup"><span data-stu-id="4850e-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="4850e-113">Der Wert 1 verhindert Änderungen am aktuellen Computer Zustand.</span><span class="sxs-lookup"><span data-stu-id="4850e-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="4850e-114">Weitere Informationen finden Sie unter [**msiopenpackageex**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="4850e-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4850e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4850e-115">Return value</span></span>

<span data-ttu-id="4850e-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4850e-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4850e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4850e-117">Remarks</span></span>

<span data-ttu-id="4850e-118">Die **OpenPackage** -Methode kann das Daten Bank handle direkt anstelle der Zeichenfolge für den Paketpfad akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4850e-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="4850e-119">Beachten Sie, dass nur ein [**Sitzungs**](session-object.md) Objekt von einem einzelnen Prozess geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4850e-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="4850e-120">**OpenPackage** kann nicht in einer benutzerdefinierten Aktion verwendet werden, da die aktive Installation die einzige zulässige Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="4850e-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="4850e-121">Ein sicheres [**Sitzungs**](session-object.md) Objekt ignoriert den aktuellen Computer Zustand beim Öffnen des Pakets und verhindert Änderungen am aktuellen Computer Status.</span><span class="sxs-lookup"><span data-stu-id="4850e-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="4850e-122">Weitere Informationen finden Sie unter [**msiopenpackageex**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="4850e-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="4850e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4850e-123">Requirements</span></span>



| <span data-ttu-id="4850e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4850e-124">Requirement</span></span> | <span data-ttu-id="4850e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4850e-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4850e-126">Version</span><span class="sxs-lookup"><span data-stu-id="4850e-126">Version</span></span><br/> | <span data-ttu-id="4850e-127">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4850e-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4850e-128">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4850e-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4850e-129">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="4850e-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4850e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4850e-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="4850e-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4850e-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4850e-132">IID</span><span class="sxs-lookup"><span data-stu-id="4850e-132">IID</span></span><br/>     | <span data-ttu-id="4850e-133">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4850e-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




