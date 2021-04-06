---
title: C-Eigenschaften. CPP
description: In der Beispiel Anbieter Komponente ist ein Beispiel für eine Implementierung des Eigenschafts Caches in "crequicpp" zu finden. In der folgenden Tabelle sind die unterstützten Methoden aufgeführt.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855332"
---
# <a name="cpropscpp"></a><span data-ttu-id="35da8-104">C-Eigenschaften. CPP</span><span class="sxs-lookup"><span data-stu-id="35da8-104">CPROPS.CPP</span></span>

<span data-ttu-id="35da8-105">In der Beispiel Anbieter Komponente ist ein Beispiel für eine Implementierung des Eigenschafts Caches in "crequicpp" zu finden.</span><span class="sxs-lookup"><span data-stu-id="35da8-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="35da8-106">In der folgenden Tabelle sind die unterstützten Methoden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="35da8-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="35da8-107">Methode</span><span class="sxs-lookup"><span data-stu-id="35da8-107">Method</span></span>                                           | <span data-ttu-id="35da8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35da8-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35da8-109">**Cpropertycache:: AddProperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="35da8-110">Erweitern Sie den Eigenschaften Cache durch Hinzufügen eines neuen.</span><span class="sxs-lookup"><span data-stu-id="35da8-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="35da8-111">**Cpropertycache:: updateproperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="35da8-112">Suchen Sie die-Eigenschaft, und verwenden Sie den Inhalt, und verwenden Sie stattdessen neue Werte. Markieren Sie dann den Cache, der für diese Eigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="35da8-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="35da8-113">**Cpropertycache:: FindProperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="35da8-114">Diese Eigenschaft nach Name suchen; Speichern Sie den Index.</span><span class="sxs-lookup"><span data-stu-id="35da8-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="35da8-115">**Cpropertycache:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="35da8-116">Suchen Sie die Eigenschaft im Cache, falls verfügbar, und wenden Sie andernfalls **GetInfo** an.</span><span class="sxs-lookup"><span data-stu-id="35da8-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="35da8-117">Legen Sie den Index fest, und kopieren Sie die neuen Werte.</span><span class="sxs-lookup"><span data-stu-id="35da8-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="35da8-118">**Cpropertycache::p utproperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="35da8-119">Suchen Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="35da8-119">Find the property.</span></span> <span data-ttu-id="35da8-120">Geben Sie an, was vorhanden ist, und geben Sie neue Werte ein.</span><span class="sxs-lookup"><span data-stu-id="35da8-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="35da8-121">**Cpropertycache:: cpropertycache**</span><span class="sxs-lookup"><span data-stu-id="35da8-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="35da8-122">Standardkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="35da8-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="35da8-123">**Cpropertycache:: ~ cpropertycache**</span><span class="sxs-lookup"><span data-stu-id="35da8-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="35da8-124">Standardedekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="35da8-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="35da8-125">**Cpropertycache:: kreatepropertycache**</span><span class="sxs-lookup"><span data-stu-id="35da8-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="35da8-126">Erstellen Sie den Cache.</span><span class="sxs-lookup"><span data-stu-id="35da8-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="35da8-127">**Cpropertycache:: unboundgetproperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="35da8-128">Suchen Sie die Eigenschaft im Cache, und legen Sie Sie auf diese Werte fest.</span><span class="sxs-lookup"><span data-stu-id="35da8-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="35da8-129">**Cpropertycache:: sampledsmarshallproperties**</span><span class="sxs-lookup"><span data-stu-id="35da8-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="35da8-130">Mars Hallen von Eigenschaften Daten und-Werten.</span><span class="sxs-lookup"><span data-stu-id="35da8-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="35da8-131">**Cpropertycache:: marshallproperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="35da8-132">Marshallt eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="35da8-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="35da8-133">**Cpropertycache:: sampledsunmarshallproperties**</span><span class="sxs-lookup"><span data-stu-id="35da8-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="35da8-134">Marshalling von Eigenschaften Daten und-Werten.</span><span class="sxs-lookup"><span data-stu-id="35da8-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="35da8-135">**Cpropertycache:: unmarshallproperty**</span><span class="sxs-lookup"><span data-stu-id="35da8-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="35da8-136">Marshalling einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="35da8-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




