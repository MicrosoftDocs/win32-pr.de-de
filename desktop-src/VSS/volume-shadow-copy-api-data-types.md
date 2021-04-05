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
# <a name="volume-shadow-copy-api-data-types"></a>Datentypen der Volumeschattenkopie-API

Die folgenden Datentypen sind in der Volumeschattenkopie-API definiert:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>VSS- \_ ID
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

Die **VSS- \_ ID** -Definition gibt das allgemeine VSS-Bezeichnerformat an. Die **VSS- \_ ID** ist ein GUID-Standard Datentyp.

**VSS \_ ID** s werden verwendet, um Folgendes zu identifizieren: Schatten Kopien, schattenkopiesätze, Anbieter, Anbieter Versionen, Schreiber (Writer-Klassen Bezeichner) und Instanzen von Writern.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ Pwsz
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

Die **VSS- \_ Pwsz** -Definition gibt eine NULL-terminierte breit Zeichen Zeichenfolge (WChar) an.

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS- \_ Zeitstempel
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

Die **VSS \_** -Zeitstempel Definition enthält Zeitstempel Informationen als einen ganzzahligen 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle seit dem 1. Januar 1601 (UTC) enthält. Diese Definition ist mit der [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur austauschbar.

</dd> </dl>

 

 
