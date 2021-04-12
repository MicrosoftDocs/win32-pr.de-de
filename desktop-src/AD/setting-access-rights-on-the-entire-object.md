---
title: Festlegen von Zugriffsrechten für das gesamte Objekt
description: Bestimmte Berechtigungen können nur für ein gesamtes Objekt festgelegt werden, z. b. für DELETE-und List-Inhalte. Vorgangs spezifische Berechtigungen, z. b. die Read-Berechtigung, können auch für das gesamte Objekt festgelegt werden, sodass Sie für ein gesamtes Objekt gelten.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Festlegen von Zugriffsrechten für das gesamte Objekt AD
- Objekte AD, Festlegen von Zugriffsrechten für
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472461"
---
# <a name="setting-access-rights-on-the-entire-object"></a><span data-ttu-id="1a64d-106">Festlegen von Zugriffsrechten für das gesamte Objekt</span><span class="sxs-lookup"><span data-stu-id="1a64d-106">Setting Access Rights on the Entire Object</span></span>

<span data-ttu-id="1a64d-107">Bestimmte Berechtigungen können nur für ein gesamtes Objekt festgelegt werden, z. b. für DELETE-und List-Inhalte.</span><span class="sxs-lookup"><span data-stu-id="1a64d-107">Certain permissions can be set only for an entire object, such as Delete and List Contents.</span></span> <span data-ttu-id="1a64d-108">Vorgangs spezifische Berechtigungen, z. b. die Read-Berechtigung, können auch für das gesamte Objekt festgelegt werden, sodass Sie für ein gesamtes Objekt gelten.</span><span class="sxs-lookup"><span data-stu-id="1a64d-108">Operation-specific permissions, such as the Read permission, can also be set for entire object so that they apply to an entire object.</span></span>

<span data-ttu-id="1a64d-109">Das folgende Verfahren kann verwendet werden, um Berechtigungen für ein gesamtes Objekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1a64d-109">The following procedure can be used to set permissions for an entire object.</span></span>

<span data-ttu-id="1a64d-110">**So legen Sie Berechtigungen für ein gesamtes Objekt fest**</span><span class="sxs-lookup"><span data-stu-id="1a64d-110">**To set permissions for an entire object**</span></span>

1.  <span data-ttu-id="1a64d-111">Legen Sie [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf ADS für den Zugriff auf den Zugriff auf den Zugriff auf den Zugriff auf AD- **\_ AceType \_ \_** **fest. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1a64d-111">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED** or **ADS\_ACETYPE\_ACCESS\_DENIED**.</span></span>
2.  <span data-ttu-id="1a64d-112">Legen Sie [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) und **IADsAccessControlEntry. eritedobjecttype** auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="1a64d-112">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) and **IADsAccessControlEntry.InheritedObjectType** to **NULL**.</span></span>

<span data-ttu-id="1a64d-113">Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="1a64d-113">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="1a64d-114">Weitere Informationen und ein Codebeispiel, das zum Festlegen eines ACE verwendet werden kann, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="1a64d-114">For more information and a code example that can be used to set an ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 