---
title: Cenum NS. CPP
description: In der Beispiel Anbieter Komponente verwendet die-Enumeration eines Namespace-Objekts die-Methoden von cenumns. cpp, die in der folgenden Tabelle aufgeführt sind.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340938"
---
# <a name="cenumnscpp"></a><span data-ttu-id="6d582-103">Cenum NS. CPP</span><span class="sxs-lookup"><span data-stu-id="6d582-103">CENUMNS.CPP</span></span>

<span data-ttu-id="6d582-104">In der Beispiel Anbieter Komponente verwendet die-Enumeration eines Namespace-Objekts die-Methoden von cenumns. cpp, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6d582-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="6d582-105">Methode</span><span class="sxs-lookup"><span data-stu-id="6d582-105">Method</span></span>                                              | <span data-ttu-id="6d582-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d582-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d582-107">**Csampledsnamespaceenum:: Create**</span><span class="sxs-lookup"><span data-stu-id="6d582-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="6d582-108">Erstellen Sie ein-Objekt, um die Enumeration eines ADS-Namespace Objekts zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="6d582-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="6d582-109">**Csampledsnamespaceenum:: csampledsnamespaceenum**</span><span class="sxs-lookup"><span data-stu-id="6d582-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="6d582-110">Standardkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="6d582-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="6d582-111">**Csampledsnamespaceenum:: ~ csampledsnamespaceenum**</span><span class="sxs-lookup"><span data-stu-id="6d582-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="6d582-112">Standardedekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="6d582-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="6d582-113">**Csampledsnamespaceenum:: Next**</span><span class="sxs-lookup"><span data-stu-id="6d582-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="6d582-114">Ruft die angegebene Anzahl von Elementen aus dem angegebenen Namespace Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6d582-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="6d582-115">**Csampledsnamespaceenum:: enumubjects**</span><span class="sxs-lookup"><span data-stu-id="6d582-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="6d582-116">Verwaltet das Abrufen der Schnittstellen Zeiger auf die-Objekte.</span><span class="sxs-lookup"><span data-stu-id="6d582-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="6d582-117">**Csampledsnamespaceenum:: fetchobjects**</span><span class="sxs-lookup"><span data-stu-id="6d582-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="6d582-118">Rufen Sie den Satz der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="6d582-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="6d582-119">**Csampledsnamespaceenum:: fetchnextobject**</span><span class="sxs-lookup"><span data-stu-id="6d582-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="6d582-120">Rufen Sie das nächste-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6d582-120">Fetch the next object.</span></span> <span data-ttu-id="6d582-121">Wenn Sie gefunden wird, erstellen Sie ein generisches Active Directory Objekt, und rufen Sie dessen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Zeiger ab</span><span class="sxs-lookup"><span data-stu-id="6d582-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 