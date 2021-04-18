---
description: Registriert einen Computer in einer Zertifikat Hierarchie mithilfe einer Vorlage, eines Zertifikat anzeigen Amens und der Zertifikat Beschreibung.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: Registrierungs simplemachinecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357840"
---
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="88b40-103">Registrierungs simplemachinecert</span><span class="sxs-lookup"><span data-stu-id="88b40-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="88b40-104">Das Beispiel "registrisimplemachinecert" registriert einen Computer in einer Zertifikat Hierarchie, indem eine Vorlage, ein Zertifikat Anzeige Name und die Zertifikat Beschreibung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88b40-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="88b40-105">Standort</span><span class="sxs-lookup"><span data-stu-id="88b40-105">Location</span></span>

<span data-ttu-id="88b40-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird eine C++-Version des Beispiels standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC \\ registrisimplemachinecert installiert.</span><span class="sxs-lookup"><span data-stu-id="88b40-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="88b40-107">Eine VBScript-Version ist im Ordner " *% Program Files%* \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VB Registrierungs \\ simplemachinecert" installiert.</span><span class="sxs-lookup"><span data-stu-id="88b40-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="88b40-108">Diskussion</span><span class="sxs-lookup"><span data-stu-id="88b40-108">Discussion</span></span>

<span data-ttu-id="88b40-109">Das Beispiel "registrisimplemachinecert":</span><span class="sxs-lookup"><span data-stu-id="88b40-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="88b40-110">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="88b40-110">Processes the command line arguments.</span></span> <span data-ttu-id="88b40-111">Die Befehlszeile muss den Namen der Vorlage, einen Zertifikat anzeigen Amen und eine Zertifikat Beschreibung enthalten.</span><span class="sxs-lookup"><span data-stu-id="88b40-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="88b40-112">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt und initialisiert es mithilfe der in der Befehlszeile angegebenen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="88b40-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="88b40-113">Der ContextAdministratorForceMachine-Wert für den ersten Parameter gibt an, dass das Zertifikat von einem Administrator angefordert wird, der im Auftrag eines Computers agiert.</span><span class="sxs-lookup"><span data-stu-id="88b40-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="88b40-114">Fügt dem Registrierungs Objekt den anzeigen Amen und die Beschreibung hinzu.</span><span class="sxs-lookup"><span data-stu-id="88b40-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="88b40-115">Versucht, die Zertifikat Anforderung zu registrieren und den Status des Prozesses zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="88b40-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="88b40-116">Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="88b40-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88b40-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88b40-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88b40-118">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="88b40-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



