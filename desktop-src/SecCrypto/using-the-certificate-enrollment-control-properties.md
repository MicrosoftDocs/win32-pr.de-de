---
description: Jede Zertifikat Registrierungs Steuerungs Eigenschaft ist Lese-/Schreibzugriff und verfügt über einen initialisierten Standardwert sowie einen Satz zulässiger Werte.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Verwenden der Eigenschaften der Zertifikat Registrierungs Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753433"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="516cb-103">Verwenden der Eigenschaften der Zertifikat Registrierungs Steuerung</span><span class="sxs-lookup"><span data-stu-id="516cb-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="516cb-104">Jede Zertifikat Registrierungs Steuerungs Eigenschaft ist Lese-/Schreibzugriff und verfügt über einen initialisierten Standardwert sowie einen Satz zulässiger Werte.</span><span class="sxs-lookup"><span data-stu-id="516cb-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="516cb-105">Sie können eine Eigenschaft auf einen beliebigen Wert in dieser Gruppe festlegen, um das Verhalten von Methoden zu ändern, die die-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="516cb-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="516cb-106">Um ein gewünschtes Verhalten zu erzielen, legen Sie die-Eigenschaft fest, bevor Sie die-Methode mit dem Wert dieser Eigenschaft aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="516cb-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="516cb-107">Beachten Sie jedoch, dass nach dem Aufrufen der folgenden Methoden</span><span class="sxs-lookup"><span data-stu-id="516cb-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="516cb-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="516cb-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="516cb-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="516cb-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="516cb-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="516cb-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="516cb-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="516cb-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="516cb-112">die zurück setzung der folgenden Eigenschaften ist blockiert.</span><span class="sxs-lookup"><span data-stu-id="516cb-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="516cb-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="516cb-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="516cb-114">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="516cb-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="516cb-115">**Providerflags**</span><span class="sxs-lookup"><span data-stu-id="516cb-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="516cb-116">**Container Name**</span><span class="sxs-lookup"><span data-stu-id="516cb-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="516cb-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="516cb-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="516cb-118">es sei denn, die [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) -Methode wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="516cb-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="516cb-119">Informationen zu einzelnen Eigenschaften und Methoden finden Sie in den Referenz Themen zu den Eigenschaften und Methoden in der [kryptografiereferenz](cryptography-reference.md).</span><span class="sxs-lookup"><span data-stu-id="516cb-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="516cb-120">Die folgenden Abschnitte enthalten sprachspezifische Informationen zum Festlegen und Abrufen der Eigenschaften der Zertifikat Registrierungs Steuerung:</span><span class="sxs-lookup"><span data-stu-id="516cb-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="516cb-121">Eigenschaften der Zertifikat Registrierungs Steuerung in C++</span><span class="sxs-lookup"><span data-stu-id="516cb-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
