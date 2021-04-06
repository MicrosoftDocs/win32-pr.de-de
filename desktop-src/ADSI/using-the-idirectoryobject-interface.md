---
title: Verwenden der IDirectoryObject-Schnittstelle
description: Wenn Sie in C oder C++ einen ADSI-Client erstellen, der eine frühe Bindung verwendet, verfügen Sie über eine größere Anzahl von ADSI-Datentypen, die für den Client verwendet werden können, wenn die IDirectoryObject-Schnittstelle anstelle der IADs-Schnittstelle aufgerufen wird.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, using
- ADSI ADSI, using, mithilfe der IDirectoryObject-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707356"
---
# <a name="using-the-idirectoryobject-interface"></a><span data-ttu-id="5c6f3-105">Verwenden der IDirectoryObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5c6f3-105">Using the IDirectoryObject Interface</span></span>

<span data-ttu-id="5c6f3-106">Wenn Sie in C oder C++ einen ADSI-Client erstellen, der eine frühe Bindung verwendet, verfügen Sie über eine größere Anzahl von ADSI-Datentypen, die für den Client verwendet werden können, wenn die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle anstelle der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-106">When you create an ADSI client in C or C++ that uses early binding, you will have a wider variety of ADSI data types available to use for your client if it calls the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface instead of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="5c6f3-107">Die **IDirectoryObject** -Schnittstelle stellt Methoden bereit, um eine Teilmenge der Wartungs Eigenschaften eines Objekts und den Zugriff auf seine Attribute zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-107">The **IDirectoryObject** interface provides methods to support a subset of an object's maintenance properties and to access its attributes.</span></span> <span data-ttu-id="5c6f3-108">Die folgende Abbildung zeigt die Beziehungen zwischen den Datenstrukturen.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-108">The following figure shows the relationships among the data structures.</span></span>

![IDirectoryObject-Schnittstellen-Datenstrukturen](images/ds2dso.png)

<span data-ttu-id="5c6f3-110">In der obigen Abbildung werden in der Struktur [**ADS \_ Objekt \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_object_info) Eigenschaften definiert, die das Objekt nach dem Distinguished Name, dem relativen Distinguished Name, by Container (parameterdn), dem Objekttyp (classdn) und der Schema Definition (schemadn) identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-110">In the preceding figure, the structure [**ADS\_OBJECT\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) defines properties that identify the object by distinguished name, relative distinguished name, by container (ParentDN), by object type (ClassDN), and by schema definition (SchemaDN).</span></span> <span data-ttu-id="5c6f3-111">Der Attribut Deskriptor [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) besteht aus einem Namen, einem Datentyp, einem Array von Datenwerten, das in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)angezeigt wird, und einem Flag, das den zugrunde liegenden Verzeichnisdienst anweist, bestimmte Vorgänge für die in [ADS \_ attr- \_ \* Konstanten](adsi-constants.md)beschriebenen Attribute auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-111">The attribute descriptor [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consists of a name, data type, an array of data values shown in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue), and a flag that directs the underlying directory service to perform certain operations on the attributes detailed in [ADS\_ATTR\_\* constants](adsi-constants.md).</span></span> <span data-ttu-id="5c6f3-112">Zu den Datentypen für diese Attribute gehören die erweiterten ADSI-Syntax Typen, die in [**adstyetenum**](/windows/win32/api/iads/ne-iads-adstypeenum)ausführlich erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="5c6f3-112">The data types for these attributes include the ADSI extended syntax types, detailed in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span></span>

 

 




