---
title: Itsremoteprogram-Schnittstelle
description: Enthält Methoden zum Festlegen und Abrufen des RemoteApp-Modus und der Startparameter für ein RemoteApp-Programm, z. b. den Pfad der ausführbaren Datei und das Arbeitsverzeichnis.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Itsremoteprogram-Schnittstelle Remotedesktopdienste
- Itsremoteprogram-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040749"
---
# <a name="itsremoteprogram-interface"></a><span data-ttu-id="17abd-105">Itsremoteprogram-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="17abd-105">ITSRemoteProgram interface</span></span>

<span data-ttu-id="17abd-106">Enthält Methoden zum Festlegen und Abrufen des RemoteApp-Modus und der Startparameter für ein RemoteApp-Programm, z. b. den Pfad der ausführbaren Datei und das Arbeitsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="17abd-106">Includes methods to set and retrieve the RemoteApp mode and the start-up parameters for a RemoteApp program, such as the path of the executable file and the working directory.</span></span>

## <a name="members"></a><span data-ttu-id="17abd-107">Member</span><span class="sxs-lookup"><span data-stu-id="17abd-107">Members</span></span>

<span data-ttu-id="17abd-108">Die **itsremoteprogram** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="17abd-108">The **ITSRemoteProgram** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="17abd-109">**Itsremoteprogram** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17abd-109">**ITSRemoteProgram** also has these types of members:</span></span>

-   [<span data-ttu-id="17abd-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="17abd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="17abd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17abd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17abd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="17abd-112">Methods</span></span>

<span data-ttu-id="17abd-113">Die Schnittstelle **itsremoteprogram** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="17abd-113">The **ITSRemoteProgram** interface has these methods.</span></span>



| <span data-ttu-id="17abd-114">Methode</span><span class="sxs-lookup"><span data-stu-id="17abd-114">Method</span></span>                                                            | <span data-ttu-id="17abd-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17abd-115">Description</span></span>                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="17abd-116">**Serverstartprogram**</span><span class="sxs-lookup"><span data-stu-id="17abd-116">**ServerStartProgram**</span></span>](itsremoteprogram-serverstartprogram.md) | <span data-ttu-id="17abd-117">Gibt ein RemoteApp-Programm an, das in der Remote Sitzung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17abd-117">Specifies a RemoteApp program to start in the remote session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="17abd-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17abd-118">Properties</span></span>

<span data-ttu-id="17abd-119">Die Schnittstelle **itsremoteprogram** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17abd-119">The **ITSRemoteProgram** interface has these properties.</span></span>



| <span data-ttu-id="17abd-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="17abd-120">Property</span></span>                                                                   | <span data-ttu-id="17abd-121">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="17abd-121">Access type</span></span>           | <span data-ttu-id="17abd-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17abd-122">Description</span></span>                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [<span data-ttu-id="17abd-123">**Remoteprogrammode**</span><span class="sxs-lookup"><span data-stu-id="17abd-123">**RemoteProgramMode**</span></span>](itsremoteprogram-remoteprogrammode.md)<br/> | <span data-ttu-id="17abd-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="17abd-124">Read/write</span></span><br/> | <span data-ttu-id="17abd-125">Der RemoteApp-Modus.</span><span class="sxs-lookup"><span data-stu-id="17abd-125">The RemoteApp mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17abd-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17abd-126">Requirements</span></span>



| <span data-ttu-id="17abd-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17abd-127">Requirement</span></span> | <span data-ttu-id="17abd-128">Wert</span><span class="sxs-lookup"><span data-stu-id="17abd-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17abd-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17abd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="17abd-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17abd-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="17abd-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17abd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="17abd-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17abd-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="17abd-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="17abd-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="17abd-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17abd-134"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="17abd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="17abd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17abd-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17abd-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="17abd-137">IID</span><span class="sxs-lookup"><span data-stu-id="17abd-137">IID</span></span><br/>                      | <span data-ttu-id="17abd-138">IID \_ itsremoteprogram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.</span><span class="sxs-lookup"><span data-stu-id="17abd-138">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="17abd-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17abd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17abd-140">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="17abd-140">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="17abd-141">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="17abd-141">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

