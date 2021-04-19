---
description: Die Action-Eigenschaft kann auf die folgenden Werte festgelegt werden.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Action-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360895"
---
# <a name="action-property"></a><span data-ttu-id="c1d15-103">Action-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c1d15-103">ACTION property</span></span>

<span data-ttu-id="c1d15-104">Die **Action** -Eigenschaft kann auf die folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c1d15-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="c1d15-105">Wert</span><span class="sxs-lookup"><span data-stu-id="c1d15-105">Value</span></span>



| <span data-ttu-id="c1d15-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c1d15-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="c1d15-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1d15-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="c1d15-108"><dt>**Installieren**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d15-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="c1d15-109">Installations Aktion</span><span class="sxs-lookup"><span data-stu-id="c1d15-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="c1d15-110"><dt>**Benen**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d15-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="c1d15-111">Aktion ankündigen</span><span class="sxs-lookup"><span data-stu-id="c1d15-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="c1d15-112"><dt>**Administrator**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d15-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="c1d15-113">Administrator Aktion</span><span class="sxs-lookup"><span data-stu-id="c1d15-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="c1d15-114">Die **Action** -Eigenschaft bestimmt, welche Aktion ausgeführt werden soll, wenn ein NULL-Aktionsname für [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) oder die [**doaction-Methode**](session-doaction.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1d15-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="c1d15-115">Wenn für die **Action** -Eigenschaft kein Wert definiert ist, ruft das Installationsprogramm die [Installations Aktion](install-action.md)auf.</span><span class="sxs-lookup"><span data-stu-id="c1d15-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d15-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1d15-116">Requirements</span></span>



| <span data-ttu-id="c1d15-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1d15-117">Requirement</span></span> | <span data-ttu-id="c1d15-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c1d15-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d15-119">Version</span><span class="sxs-lookup"><span data-stu-id="c1d15-119">Version</span></span><br/> | <span data-ttu-id="c1d15-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1d15-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1d15-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1d15-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1d15-122">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c1d15-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c1d15-123">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d15-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1d15-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1d15-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d15-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1d15-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




