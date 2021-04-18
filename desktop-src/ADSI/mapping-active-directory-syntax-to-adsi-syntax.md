---
title: Zuordnung Active Directory Syntax zur ADSI-Syntax
description: In der folgenden Tabelle sind die Active Directory Syntaxen der entsprechenden ADSI-Syntax zugeordnet.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- Attribute ADSI, Mapping Active Directory Syntax zur ADSI-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340605"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="1e2af-104">Zuordnung Active Directory Syntax zur ADSI-Syntax</span><span class="sxs-lookup"><span data-stu-id="1e2af-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="1e2af-105">In der folgenden Tabelle sind die Active Directory Syntaxen der entsprechenden ADSI-Syntax zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1e2af-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="1e2af-106">Attribut Syntax-ID</span><span class="sxs-lookup"><span data-stu-id="1e2af-106">Attribute syntax ID</span></span> | <span data-ttu-id="1e2af-107">Active Directory-Syntax Typs</span><span class="sxs-lookup"><span data-stu-id="1e2af-107">Active Directory syntax type</span></span>             | <span data-ttu-id="1e2af-108">Äquivalente ADSI-Syntax Typen</span><span class="sxs-lookup"><span data-stu-id="1e2af-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1e2af-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="1e2af-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="1e2af-110">DN-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-110">DN String</span></span><br/>                     | <span data-ttu-id="1e2af-111">DN-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="1e2af-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="1e2af-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="1e2af-113">ObjectID</span><span class="sxs-lookup"><span data-stu-id="1e2af-113">Object ID</span></span><br/>                     | <span data-ttu-id="1e2af-114">Caseignore-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="1e2af-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="1e2af-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="1e2af-116">Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="1e2af-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="1e2af-117">Caseexact-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="1e2af-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="1e2af-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="1e2af-119">Case-Zeichenfolge ignoriert</span><span class="sxs-lookup"><span data-stu-id="1e2af-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="1e2af-120">Caseignore-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="1e2af-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="1e2af-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="1e2af-122">Print Case-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-122">Print Case String</span></span><br/>             | <span data-ttu-id="1e2af-123">Druckbare Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="1e2af-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="1e2af-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="1e2af-125">Numerische Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-125">Numeric String</span></span><br/>                | <span data-ttu-id="1e2af-126">Numerische Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="1e2af-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="1e2af-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="1e2af-128">**Oder** Name dnwithoctetstring</span><span class="sxs-lookup"><span data-stu-id="1e2af-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="1e2af-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1e2af-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="1e2af-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="1e2af-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="1e2af-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="1e2af-131">Boolean</span></span><br/>                       | <span data-ttu-id="1e2af-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="1e2af-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="1e2af-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="1e2af-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="1e2af-134">Integer</span><span class="sxs-lookup"><span data-stu-id="1e2af-134">Integer</span></span><br/>                       | <span data-ttu-id="1e2af-135">Integer</span><span class="sxs-lookup"><span data-stu-id="1e2af-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="1e2af-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="1e2af-136">2.5.5.10</span></span><br/> | <span data-ttu-id="1e2af-137">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-137">Octet String</span></span><br/>                  | <span data-ttu-id="1e2af-138">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="1e2af-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="1e2af-139">2.5.5.11</span></span><br/> | <span data-ttu-id="1e2af-140">Time</span><span class="sxs-lookup"><span data-stu-id="1e2af-140">Time</span></span><br/>                          | <span data-ttu-id="1e2af-141">UTC-Zeit</span><span class="sxs-lookup"><span data-stu-id="1e2af-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="1e2af-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="1e2af-142">2.5.5.12</span></span><br/> | <span data-ttu-id="1e2af-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="1e2af-143">Unicode</span></span><br/>                       | <span data-ttu-id="1e2af-144">Case-Zeichenfolge ignorieren</span><span class="sxs-lookup"><span data-stu-id="1e2af-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="1e2af-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="1e2af-145">2.5.5.13</span></span><br/> | <span data-ttu-id="1e2af-146">Adresse</span><span class="sxs-lookup"><span data-stu-id="1e2af-146">Address</span></span><br/>                       | <span data-ttu-id="1e2af-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1e2af-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="1e2af-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="1e2af-148">2.5.5.14</span></span><br/> | <span data-ttu-id="1e2af-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="1e2af-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="1e2af-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="1e2af-150">2.5.5.15</span></span><br/> | <span data-ttu-id="1e2af-151">NT-Sicherheits Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e2af-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="1e2af-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1e2af-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="1e2af-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="1e2af-153">2.5.5.16</span></span><br/> | <span data-ttu-id="1e2af-154">Große ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="1e2af-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="1e2af-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="1e2af-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="1e2af-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="1e2af-156">2.5.5.17</span></span><br/> | <span data-ttu-id="1e2af-157">SID</span><span class="sxs-lookup"><span data-stu-id="1e2af-157">SID</span></span><br/>                           | <span data-ttu-id="1e2af-158">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1e2af-158">Octet String</span></span><br/>                                             |



 

 

 





