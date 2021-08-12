---
description: 'Die folgenden Datentypen werden in der Volumeschattenkopie-API definiert:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Volumeschattenkopie-API-Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b159156c4a892ae7ad07a4d988bb8f32b0f5689a440fe3f31da3d6c15470675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590562"
---
# <a name="volume-shadow-copy-api-data-types"></a>Volumeschattenkopie-API-Datentypen

Die folgenden Datentypen werden in der Volumeschattenkopie-API definiert:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>\_VSS-ID
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

Die **\_ VSS-ID-Definition** gibt das allgemeine VSS-Bezeichnerformat an. Die **\_ VSS-ID** ist ein GUID-Standarddatentyp.

**VSS \_ ID-Dateien** werden verwendet, um Folgendes zu identifizieren: Schattenkopien, Schattenkopiesätze, Anbieter, Anbieterversionen, Writer (Klassenbezeichner des Autors) und Instanzen von Writern.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ PWSZ
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

Die **VSS \_ PWSZ-Definition** gibt eine nullendte Breitzeichenfolge (wchar) an.

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_VSS-ZEITSTEMPEL
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

Die **VSS \_ TIMESTAMP-Definition** enthält Zeitstempelinformationen als 64-Bit-Ganzzahlwert, der die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) enthält. Diese Definition kann mit der [**FILETIME-Struktur ausgetauscht**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) werden.

</dd> </dl>

 

 
