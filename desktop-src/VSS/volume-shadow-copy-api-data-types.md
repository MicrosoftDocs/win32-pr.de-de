---
description: 'Die folgenden Datentypen sind in der Volumeschattenkopie-API definiert:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Datentypen der Volumeschattenkopie-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751584"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="fa03d-103">Datentypen der Volumeschattenkopie-API</span><span class="sxs-lookup"><span data-stu-id="fa03d-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="fa03d-104">Die folgenden Datentypen sind in der Volumeschattenkopie-API definiert:</span><span class="sxs-lookup"><span data-stu-id="fa03d-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="fa03d-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS- \_ ID</span><span class="sxs-lookup"><span data-stu-id="fa03d-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="fa03d-106">Die **VSS- \_ ID** -Definition gibt das allgemeine VSS-Bezeichnerformat an.</span><span class="sxs-lookup"><span data-stu-id="fa03d-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="fa03d-107">Die **VSS- \_ ID** ist ein GUID-Standard Datentyp.</span><span class="sxs-lookup"><span data-stu-id="fa03d-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="fa03d-108">**VSS \_ ID** s werden verwendet, um Folgendes zu identifizieren: Schatten Kopien, schattenkopiesätze, Anbieter, Anbieter Versionen, Schreiber (Writer-Klassen Bezeichner) und Instanzen von Writern.</span><span class="sxs-lookup"><span data-stu-id="fa03d-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="fa03d-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ Pwsz</span><span class="sxs-lookup"><span data-stu-id="fa03d-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="fa03d-110">Die **VSS- \_ Pwsz** -Definition gibt eine NULL-terminierte breit Zeichen Zeichenfolge (WChar) an.</span><span class="sxs-lookup"><span data-stu-id="fa03d-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="fa03d-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS- \_ Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="fa03d-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="fa03d-112">Die **VSS \_** -Zeitstempel Definition enthält Zeitstempel Informationen als einen ganzzahligen 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle seit dem 1. Januar 1601 (UTC) enthält.</span><span class="sxs-lookup"><span data-stu-id="fa03d-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="fa03d-113">Diese Definition ist mit der [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur austauschbar.</span><span class="sxs-lookup"><span data-stu-id="fa03d-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
