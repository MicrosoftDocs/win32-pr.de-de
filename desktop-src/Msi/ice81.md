---
description: ICE81 überprüft die msidigitalcertificate-Tabelle, die msidigitalsignature-Tabelle, die MsiPatchCertificate-Tabelle und die msipackagecertificate-Tabelle.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752792"
---
# <a name="ice81"></a><span data-ttu-id="e1739-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="e1739-103">ICE81</span></span>

<span data-ttu-id="e1739-104">ICE81 überprüft die [msidigitalcertificate](msidigitalcertificate-table.md)-Tabelle, die [msidigitalsignature-Tabelle](msidigitalsignature-table.md), die [MsiPatchCertificate](msipatchcertificate-table.md)-Tabelle und die [msipackagecertificate-Tabelle](msipackagecertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1739-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="e1739-105">Durch diese benutzerdefinierte Ice-Aktion werden Warnungen für digitale Zertifikate ausgegeben, die nicht verwendet werden oder auf die nicht verwiesen wird. Außerdem wird ein Fehler ausgegeben, wenn das signierte Objekt nicht vorhanden ist oder die CAB-Datei des signierten Objekts nicht auf externe Daten zeigt.</span><span class="sxs-lookup"><span data-stu-id="e1739-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="e1739-106">Beachten Sie, dass ICE03 überprüft, ob der Eintrag in der Tabellenspalte in der msidigitalsignature-Tabelle "Media" lautet.</span><span class="sxs-lookup"><span data-stu-id="e1739-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="e1739-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="e1739-107">Result</span></span>

<span data-ttu-id="e1739-108">ICE81 gibt die folgenden Warnungen für nicht verwendete oder nicht referenzierte digitale Zertifikate aus.</span><span class="sxs-lookup"><span data-stu-id="e1739-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="e1739-109">ICE81-Warnung</span><span class="sxs-lookup"><span data-stu-id="e1739-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="e1739-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1739-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e1739-111">In den Tabellen msidigitalsignature, msipackagecertificate oder MsiPatchCertificate konnte kein Verweis auf einen der Datensätze in der Tabelle msidigitalcertificate gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e1739-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="e1739-112">Diese Warnung wird zurückgegeben, wenn alle Datensätze nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1739-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="e1739-113">\[ \] In den Tabellen msidigitalsignature, msipackagecertificate oder MsiPatchCertificate konnte kein Verweis auf das digitale Zertifikat 1 gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e1739-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="e1739-114">Diese Warnung wird zurückgegeben, wenn einige Datensätze, aber nicht alle, nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1739-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="e1739-115">ICE81 gibt die folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="e1739-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="e1739-116">ICE81-Fehler</span><span class="sxs-lookup"><span data-stu-id="e1739-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="e1739-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1739-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1739-118">Die Medien Tabelle ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1739-118">Media Table does not exist.</span></span> <span data-ttu-id="e1739-119">Daher sind alle Einträge in msidigitalsignature falsch.</span><span class="sxs-lookup"><span data-stu-id="e1739-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="e1739-120">Das signierte Objekt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1739-120">The signed object does not exist.</span></span> <span data-ttu-id="e1739-121">Dieser Fehler wird zurückgegeben, wenn die Medien Tabelle nicht vorhanden ist, aber msidigitalsignature Einträge aufweist.</span><span class="sxs-lookup"><span data-stu-id="e1739-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="e1739-122">Fehlendes signiertes Objekt \[ 2 \] in der Medien Tabelle</span><span class="sxs-lookup"><span data-stu-id="e1739-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="e1739-123">Das signierte Objekt \[ 2 \] ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1739-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="e1739-124">Dieser Fehler wird zurückgegeben, wenn die Medien Tabelle vorhanden ist, dieser Eintrag in msidigitalsignature jedoch nicht in der Medien Tabelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e1739-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="e1739-125">Der Eintrag in Tabelle \[ 1 \] mit Schlüssel \[ 2 \] wird signiert.</span><span class="sxs-lookup"><span data-stu-id="e1739-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="e1739-126">Daher sollte die CAB-Seite auf ein Objekt außerhalb des Pakets zeigen (der Wert von CAB sollte nicht mit dem Präfix versehen werden \# ).</span><span class="sxs-lookup"><span data-stu-id="e1739-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="e1739-127">Die CAB-Datei des signierten Objekts verweist nicht auf externe Daten.</span><span class="sxs-lookup"><span data-stu-id="e1739-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="e1739-128">\[1 \] ist der Tabellenname.</span><span class="sxs-lookup"><span data-stu-id="e1739-128">\[1\] is table name.</span></span> <span data-ttu-id="e1739-129">\[2 \] ist der Schlüssel in der Medien Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e1739-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="e1739-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1739-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1739-131">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="e1739-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



