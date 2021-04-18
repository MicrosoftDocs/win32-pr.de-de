---
description: Verwenden Sie certmgr, um Zertifikate, CRLs und CTLs aus einer Datei oder einem Zertifikat Speicher anzuzeigen, Zertifikate in einen Zertifikat Speicher zu kopieren, Zertifikate aus einem Zertifikat Speicher zu löschen und Zertifikate in Dateien zu speichern.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Verwenden von certmgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347250"
---
# <a name="using-certmgr"></a><span data-ttu-id="0ad1d-103">Verwenden von certmgr</span><span class="sxs-lookup"><span data-stu-id="0ad1d-103">Using CertMgr</span></span>

<span data-ttu-id="0ad1d-104">[Certmgr](certmgr.md) kann verwendet werden, um [*Zertifikate*](../secgloss/c-gly.md), [*Zertifikats Sperr Listen*](../secgloss/c-gly.md) (CRLs) und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) aus einer Datei oder einem Zertifikat Speicher anzuzeigen, Zertifikate in einen [*Zertifikat Speicher*](../secgloss/c-gly.md)zu kopieren, Zertifikate aus einem Zertifikat Speicher zu löschen und Zertifikate in Dateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="0ad1d-105">Wenn [Certmgr](certmgr.md) ohne Optionen verwendet wird, wird ein certmgr-Assistent angezeigt, der den Benutzer durch den Vorgang führt.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="0ad1d-106">Bei der Datei muss es sich um einen der folgenden Typen handeln:</span><span class="sxs-lookup"><span data-stu-id="0ad1d-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="0ad1d-107">Eine codierte CTL-, CRL-oder Zertifikatsdatei (kann Base-64-codiert sein)</span><span class="sxs-lookup"><span data-stu-id="0ad1d-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="0ad1d-108">Eine PKCS \# 7-Datei</span><span class="sxs-lookup"><span data-stu-id="0ad1d-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="0ad1d-109">Eine SPC-Datei</span><span class="sxs-lookup"><span data-stu-id="0ad1d-109">An SPC file</span></span>
-   <span data-ttu-id="0ad1d-110">Ein signiertes Dokument</span><span class="sxs-lookup"><span data-stu-id="0ad1d-110">A signed document</span></span>
-   <span data-ttu-id="0ad1d-111">Eine serialisierte StoreFile</span><span class="sxs-lookup"><span data-stu-id="0ad1d-111">A serialized storeFile</span></span>

<span data-ttu-id="0ad1d-112">In den folgenden Beispielen werden die Befehle " [Certmgr](certmgr.md) " verwendet, um allgemeine Zertifikat Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="0ad1d-113">Zeigen Sie die Zertifikate, CRLs und CTLs aus " *MyFile. ext*" an.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="0ad1d-114">**Certmgr** *MyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="0ad1d-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="0ad1d-115">Zeigen Sie die Zertifikate, CRLs und CTLs aus dem eigenen Systemspeicher an.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="0ad1d-116">**certmgr-s My**</span><span class="sxs-lookup"><span data-stu-id="0ad1d-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="0ad1d-117">Kopieren Sie alle Zertifikate, CRLs und CTLs in eine Datei mit dem Namen " *MyFile. ext* " in eine neue Datei mit dem Namen " *NewFile. ext*".</span><span class="sxs-lookup"><span data-stu-id="0ad1d-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="0ad1d-118">**Certmgr-Add-All-c** *MyFile. ext* *NewFile. ext*</span><span class="sxs-lookup"><span data-stu-id="0ad1d-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="0ad1d-119">Kopieren Sie alle Zertifikate, CRLs und CTLs aus dem eigenen Systemspeicher in eine Datei mit dem Namen *newmyfile. ext*.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="0ad1d-120">**Certmgr-Add-All-c-s My** *newmyfile. ext*</span><span class="sxs-lookup"><span data-stu-id="0ad1d-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="0ad1d-121">Kopieren Sie ein Zertifikat mit dem allgemeinen Namen *MyCert* im eigenen Systemspeicher in eine Datei mit dem Namen *newCert. CER*.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="0ad1d-122">**Certmgr-Add-c-n** *MyCert* **-s My** *newCert. CER*</span><span class="sxs-lookup"><span data-stu-id="0ad1d-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="0ad1d-123">Löschen Sie alle Zertifikate aus dem eigenen Systemspeicher.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="0ad1d-124">**certmgr-del-all-c-s My**</span><span class="sxs-lookup"><span data-stu-id="0ad1d-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="0ad1d-125">Löschen Sie alle CTLs aus dem eigenen Systemspeicher, und speichern Sie den resultierenden Speicher in einer Datei mit dem Namen *newStore. Str*.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="0ad1d-126">**certmgr-del-all-CTL-s My** *newStore. Str*</span><span class="sxs-lookup"><span data-stu-id="0ad1d-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="0ad1d-127">Speichern Sie in einer Datei mit dem Namen *newCert. CER*, einem Zertifikat, bei dem es sich um ein [*X. 509*](../secgloss/x-gly.md) -codiertes Zertifikat mit dem allgemeinen Namen *MyCert* handelt, das sich im Stamm Zertifikat Speicher befindet.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="0ad1d-128">**Certmgr-Put-c-n** *MyCert* **-s root** *newCert. CER*</span><span class="sxs-lookup"><span data-stu-id="0ad1d-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ad1d-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ad1d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad1d-130">CertMgr</span><span class="sxs-lookup"><span data-stu-id="0ad1d-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
