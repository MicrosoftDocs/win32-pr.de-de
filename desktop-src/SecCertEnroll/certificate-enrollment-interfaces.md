---
description: Die folgenden Schnittstellen können verwendet werden, um einen Benutzer oder Computer in einer Zertifikatshierarchie anzumelden.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Zertifikat Registrierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352582"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="0ce46-103">Zertifikat Registrierungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0ce46-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="0ce46-104">Die folgenden Schnittstellen können verwendet werden, um einen Benutzer oder Computer in einer Zertifikatshierarchie anzumelden.</span><span class="sxs-lookup"><span data-stu-id="0ce46-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="0ce46-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0ce46-105">Interface</span></span>                                              | <span data-ttu-id="0ce46-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ce46-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ce46-107">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="0ce46-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="0ce46-108">Registriert einen Computer oder Benutzer in einer Zertifikatshierarchie.</span><span class="sxs-lookup"><span data-stu-id="0ce46-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="0ce46-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="0ce46-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="0ce46-110">Erweitert die [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0ce46-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="0ce46-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="0ce46-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="0ce46-112">Definiert Methoden, mit denen eine Webanwendung ein Zertifikat registrieren, Anmelde Informationen für den Richtlinien Server im Anmelde Informations Cache speichern und Richtlinien Server und Registrierungs Server registrieren kann.</span><span class="sxs-lookup"><span data-stu-id="0ce46-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="0ce46-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="0ce46-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="0ce46-114">Ruft ausführliche Fehlerinformationen zu einer Zertifikat Registrierungs Transaktion ab.</span><span class="sxs-lookup"><span data-stu-id="0ce46-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="0ce46-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="0ce46-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="0ce46-116">X. 509-Schnittstelle für einfaches Computer-anmeldungprotokoll</span><span class="sxs-lookup"><span data-stu-id="0ce46-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="0ce46-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ce46-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce46-118">CertEnroll-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0ce46-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




