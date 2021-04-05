---
description: Verwenden Sie Makecert-Befehle zum Erstellen von Test Zertifikaten mithilfe der Optionen, die in Internet Explorer Version 4,0 oder höher verfügbar sind.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Verwenden von Makecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753448"
---
# <a name="using-makecert"></a><span data-ttu-id="c4cc6-103">Verwenden von Makecert</span><span class="sxs-lookup"><span data-stu-id="c4cc6-103">Using MakeCert</span></span>

<span data-ttu-id="c4cc6-104">In den folgenden Beispielen werden [Makecert](makecert.md) -Befehle zum Erstellen von Test Zertifikaten mithilfe der Optionen verwendet, die in Internet Explorer Version 4,0 oder höher verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="c4cc6-105">Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="c4cc6-106">Speichern Sie das Zertifikat in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="c4cc6-107">**Makecert** *mynew. CER*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="c4cc6-108">Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="c4cc6-109">Speichern Sie Sie in einem Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="c4cc6-110">**Makecert-SS** *mynewstore*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="c4cc6-111">Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="c4cc6-112">Erstellen Sie einen Schlüssel Container, und speichern Sie das Zertifikat in einem Geschäft und in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="c4cc6-113">**Makecert-SK** *mynewkey* **-SS** *mynewstore* *mynew. CER*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="c4cc6-114">Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="c4cc6-115">Erstellen Sie eine Datei mit einem privaten Schlüssel, und speichern Sie das Zertifikat sowohl in einem Speicher als auch in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="c4cc6-116">**Makecert-SV** *mykeyfile* **-SS** *mynewstore* *mynew. CER*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="c4cc6-117">Erstellen Sie ein Zertifikat, das vom Standardtest Stamm ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="c4cc6-118">Erstellen Sie einen Schlüssel Container, speichern Sie das Zertifikat in einem Geschäft und in einer Datei, und machen Sie den privaten Schlüssel exportierbar.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="c4cc6-119">**Makecert-SK** *mynewkey* **-SS** *mynewstore* *mynew. CER* **-PE**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="c4cc6-120">Erstellen Sie ein Zertifikat mit dem Standardtest Stamm.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="c4cc6-121">Speichern Sie das Zertifikat in einem Speicher.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-121">Save the certificate to a store.</span></span> <span data-ttu-id="c4cc6-122">Erstellen Sie dann ein anderes Zertifikat, das vom neu erstellten Zertifikat ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="c4cc6-123">Speichern Sie das zweite Zertifikat in einem anderen Speicher.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="c4cc6-124">**Makecert-SK** *mynewkey* **-SS** *mynewstore* **Makecert-ist** *mynewstore* **-SS** *anotherstore*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="c4cc6-125">Erstellen Sie ein Zertifikat mit dem Standardtest Stamm.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="c4cc6-126">Speichern Sie das Zertifikat im eigenen Speicher.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="c4cc6-127">Erstellen Sie dann mithilfe des neu erstellten Zertifikats ein weiteres Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="c4cc6-128">Wenn im eigenen Speicher mehr als ein Zertifikat vorhanden ist, muss das Zertifikat mithilfe seines allgemeinen Namens identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="c4cc6-129">**Makecert-SK** *mynewkey* **-n "CN = xxzzyy"-SS My Makecert-is my-in "xxzzyy"-SS** *anotherstore*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="c4cc6-130">Erstellen Sie ein Zertifikat mit dem Standardtest Stamm.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="c4cc6-131">Speichern Sie das Zertifikat im eigenen Speicher und in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="c4cc6-132">Erstellen Sie dann mit dem neu erstellten *mynew* -Zertifikat ein anderes Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="c4cc6-133">Wenn im eigenen Speicher mehr als ein Zertifikat vorhanden ist, identifizieren Sie das erste Zertifikat mit dem Namen der Zertifikat Datei eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="c4cc6-134">**Makecert-SK** *mynewkey* **-n "CN = xxzzyy"-SS My** *mynew. CER* **Makecert-ist My-IC** *mynew. CER* **-SS** *anotherstore*</span><span class="sxs-lookup"><span data-stu-id="c4cc6-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



