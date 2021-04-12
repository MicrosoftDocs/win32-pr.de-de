---
description: Nicht-Berechnungs-Counter-Typen verfügen nicht über eine zugeordnete Formel. Der Rohwert ist von Bedeutung.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Nicht-Berechnungs-Counter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216897"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="1a593-104">Nicht-Berechnungs-Counter-Typen</span><span class="sxs-lookup"><span data-stu-id="1a593-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="1a593-105">Nicht-Berechnungs-Counter-Typen verfügen nicht über eine zugeordnete Formel.</span><span class="sxs-lookup"><span data-stu-id="1a593-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="1a593-106">Der Rohwert ist von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="1a593-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="1a593-107">Die **filestobeindexed** -Eigenschaft in der [**Win32 \_ perfrawdata \_ ContentIndex \_ indexingservice**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) -Klasse ist ein Beispiel für den Leistungsindikator " **\_ \_ rawcount** Counter Type".</span><span class="sxs-lookup"><span data-stu-id="1a593-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="1a593-108">Sie enthält eine Anzahl von Dateien, die nicht indiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="1a593-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="1a593-109">Leistungsdaten Typen werden durch die in Winperf. h definierte Konstante festgelegt, die sich im Microsoft Windows Software Development Kit (SDK) befindet.</span><span class="sxs-lookup"><span data-stu-id="1a593-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1a593-110">In der folgenden Tabelle sind die bereitgestellten nicht Berechnungs Typen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a593-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="1a593-111">Counter Type</span><span class="sxs-lookup"><span data-stu-id="1a593-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="1a593-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a593-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a593-113">Leistung [ \_ Counter- \_ Text](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span><span class="sxs-lookup"><span data-stu-id="1a593-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="1a593-114">Dieser zähtertyp zeigt eine Text Zeichenfolge variabler Länge in Unicode an.</span><span class="sxs-lookup"><span data-stu-id="1a593-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="1a593-115">Berechnete Werte werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a593-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="1a593-116">Leistung [ \_ Zähler \_ rawcount](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span><span class="sxs-lookup"><span data-stu-id="1a593-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="1a593-117">Der Rohdaten Wert, der keine Berechnungen erfordert, und stellt ein Beispiel dar, bei dem es sich nur um den zuletzt beobachteten Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="1a593-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="1a593-118">Leistung [ \_ Zähler \_ Large \_ rawcount](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span><span class="sxs-lookup"><span data-stu-id="1a593-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="1a593-119">Identisch mit dem Leistungs **\_ Zähler \_ rawcount**, aber eine 64-Bit-Darstellung für größere Werte.</span><span class="sxs-lookup"><span data-stu-id="1a593-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="1a593-120">Leistung [ \_ Zähler \_ rawcount \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="1a593-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="1a593-121">Zuletzt beobachteter Wert im Hexadezimal Format.</span><span class="sxs-lookup"><span data-stu-id="1a593-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="1a593-122">Er zeigt keinen Durchschnittswert an.</span><span class="sxs-lookup"><span data-stu-id="1a593-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="1a593-123">Leistung [ \_ Zähler \_ Large \_ rawcount \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span><span class="sxs-lookup"><span data-stu-id="1a593-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="1a593-124">Identisch mit dem Leistungs **\_ Zähler \_ rawcount \_ Hex**, aber eine 64-Bit-Darstellung im Hexadezimal Format für die Verwendung mit großen Werten.</span><span class="sxs-lookup"><span data-stu-id="1a593-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1a593-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a593-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a593-126">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="1a593-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

