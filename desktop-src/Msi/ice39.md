---
description: ICE39 überprüft den Zusammenfassungs Informationsdaten Strom der Datenbank.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358566"
---
# <a name="ice39"></a><span data-ttu-id="d48f2-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="d48f2-103">ICE39</span></span>

<span data-ttu-id="d48f2-104">ICE39 überprüft den [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d48f2-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="d48f2-105">ICE39 überprüft das Format der folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d48f2-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="d48f2-106">**Zusammenfassung der Wort Zählung**</span><span class="sxs-lookup"><span data-stu-id="d48f2-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="d48f2-107">**Zusammenfassung der Seitenanzahl**</span><span class="sxs-lookup"><span data-stu-id="d48f2-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="d48f2-108">**Vorlagen Zusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="d48f2-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="d48f2-109">**Zusammenfassung der Revisionsnummer**</span><span class="sxs-lookup"><span data-stu-id="d48f2-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="d48f2-110">**Zeit-/datezusammenfassung erstellen**</span><span class="sxs-lookup"><span data-stu-id="d48f2-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="d48f2-111">**Zusammenfassung der letzten gespeicherten Zeit/Datum**</span><span class="sxs-lookup"><span data-stu-id="d48f2-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="d48f2-112">**Letzte gedruckte Zusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="d48f2-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="d48f2-113">Wenn die Eigenschaft für die [**Wort Zähl Zusammenfassung**](word-count-summary.md) angibt, dass die Quelle komprimiert ist, gibt ICE39 eine Warnung aus, wenn in der Spalte Attribute der [Dateitabelle](file-table.md)auch Dateien als komprimiert gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d48f2-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="d48f2-114">Siehe [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="d48f2-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="d48f2-115">ICE39 gibt eine Warnung aus, wenn die [**Wort Zählung-Zusammenfassungs**](word-count-summary.md) Eigenschaft angibt, dass das Paket UAC-kompatibel ist und die [msipackagecertificate-Tabelle](msipackagecertificate-table.md) nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="d48f2-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d48f2-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d48f2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d48f2-117">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="d48f2-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



