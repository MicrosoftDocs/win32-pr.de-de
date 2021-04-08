---
title: Access Control-und Schreibvorgänge
description: Eigenschafts Änderungen schlagen fehl, wenn der Aufrufer nicht über ausreichende Rechte verfügt.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- Access Control-und Writer-Vorgänge AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858113"
---
# <a name="access-control-and-write-operations"></a><span data-ttu-id="096b0-104">Access Control-und Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="096b0-104">Access Control and Write Operations</span></span>

<span data-ttu-id="096b0-105">Eigenschafts Änderungen schlagen fehl, wenn der Aufrufer nicht über ausreichende Rechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="096b0-105">Property modifications fail if the caller does not have sufficient rights.</span></span> <span data-ttu-id="096b0-106">Bei Schreibvorgängen, bei denen Änderungen an mehreren Eigenschaften in Batches ausgeführt werden, schlägt der gesamte Vorgang fehl, wenn der Aufrufer nicht über die erforderlichen Rechte für eine einzelne der geänderten Eigenschaften verfügt.</span><span class="sxs-lookup"><span data-stu-id="096b0-106">For write operations that batch modifications to multiple properties, the entire operation fails if the caller does not have the necessary rights to a single one of the modified properties.</span></span> <span data-ttu-id="096b0-107">Beispielsweise können Sie mehrere [**IADs erstellen::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Aufrufe, um mehrere Eigenschaften für ein Objekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="096b0-107">For example, you can make multiple [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) calls to set multiple properties on an object.</span></span> <span data-ttu-id="096b0-108">Wenn Sie jedoch " [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) " aufrufen, um die neuen Daten aus dem lokalen Cache in das Verzeichnis zu schreiben, schlägt " **stinfo** " fehl, wenn der Aufrufer keinen Schreibzugriff auf alle geänderten Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="096b0-108">However, when you call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to write the new data from the local cache to the directory, **SetInfo** will fail if the caller does not have write access to all the modified properties.</span></span> <span data-ttu-id="096b0-109">Ebenso kann die [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) -Methode keine Eigenschaften festlegen, wenn der Aufrufer keinen Zugriff auf alle Eigenschaften hat, die festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="096b0-109">Similarly, the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method fails to set any properties if the caller does not have access to all the properties being set.</span></span> <span data-ttu-id="096b0-110">Daher sollten Sie mehrere Änderungs Vorgänge nur dann in Batches Verpacken, wenn Sie wissen, dass alle Änderungen erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="096b0-110">So you should batch multiple modify operations only if you know that all modifications will succeed.</span></span> <span data-ttu-id="096b0-111">Um die Attribute eines Verzeichnis Objekts zu ermitteln, das der Aufrufer ändern kann, lesen Sie das Attribut " **attributedattributeseffective** " des Objekts.</span><span class="sxs-lookup"><span data-stu-id="096b0-111">To determine the attributes of a directory object that the caller has the ability to modify, read the object's **allowedAttributesEffective** attribute.</span></span>

<span data-ttu-id="096b0-112">Wenn der Aufrufer nicht über ausreichende Rechte verfügt, um eine Eigenschaft zu ändern, können die folgenden Rückgabecodes zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="096b0-112">If the caller does not have sufficient rights to modify a property, the following return codes may be returned:</span></span>

<span data-ttu-id="096b0-113">e \_ ADS- \_ Eigenschaft \_ nicht \_ festgelegt e \_ ADS- \_ Eigenschaft \_ nicht \_ geändert</span><span class="sxs-lookup"><span data-stu-id="096b0-113">E\_ADS\_PROPERTY\_NOT\_SET E\_ADS\_PROPERTY\_NOT\_MODIFIED</span></span>

 

 