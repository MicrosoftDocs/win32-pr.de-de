---
description: In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von PFX-Nachrichten (Personal Information Exchange) exportiert wird.
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funktionen für den persönlichen Informationsaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352210"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="471c7-103">Funktionen für den persönlichen Informationsaustausch</span><span class="sxs-lookup"><span data-stu-id="471c7-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="471c7-104">In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von PFX-Nachrichten (Personal Information Exchange) exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="471c7-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="471c7-105">Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht.</span><span class="sxs-lookup"><span data-stu-id="471c7-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="471c7-106">"kreatefilepfxwstr"</span><span class="sxs-lookup"><span data-stu-id="471c7-106">createFilePFXWStr</span></span>

<span data-ttu-id="471c7-107">Die [**Funktion "**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) Funktion in Xenroll.dll" speichert eine Zertifikat Kette und einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) in einer Datei im PFX-Format.</span><span class="sxs-lookup"><span data-stu-id="471c7-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="471c7-108">Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Kopieren der PFX-Nachricht in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="471c7-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="471c7-109">Sie können jedoch [**die Methode "**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) Methode" in der [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle verwenden, um eine codierte PFX-Nachricht zu erstellen und eine benutzerdefinierte Funktion zum Speichern der Nachricht in einer Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="471c7-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="471c7-110">"kreatepfxwstr"</span><span class="sxs-lookup"><span data-stu-id="471c7-110">createPFXWStr</span></span>

<span data-ttu-id="471c7-111">Die Funktion " [**epatepfxwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) " in Xenroll.dll speichert eine Zertifikat Kette und einen privaten Schlüssel in einer PFX-Format Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="471c7-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="471c7-112">Sie können [**die Methode "**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) Methode" in der [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle verwenden, um eine codierte PFX-Nachricht zu erstellen, die die Zertifikatskette und den Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="471c7-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="471c7-113">Sie können ein Kennwort, Exportoptionen und den Codierungstyp angeben.</span><span class="sxs-lookup"><span data-stu-id="471c7-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="471c7-114">Um eine Zeichenfolge abzurufen, die der von " [**kreatepfxwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr)" zurückgegebenen entspricht, übergeben Sie das XCN \_ crypt-Zeichen folgen \_ \_ Binär Flag im- [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) *Codierungs* Parameter der Methode "Methode".</span><span class="sxs-lookup"><span data-stu-id="471c7-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="471c7-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="471c7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="471c7-116">Zuordnung von Xenroll.dll zu CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="471c7-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="471c7-117">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="471c7-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
