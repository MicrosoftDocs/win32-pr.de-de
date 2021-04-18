---
description: 'Die WFP-Registrierungs Werte befinden sich im folgenden Registrierungsschlüssel: HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: WFP-Registrierungs Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352527"
---
# <a name="wfp-registry-values"></a>WFP-Registrierungs Werte

\[WFP-Registrierungs Werte werden ab Windows Vista nicht unterstützt.\]

WFP verwendet mehrere Registrierungs Werte für Anpassungs Einstellungen. Die WFP-Registrierungs Werte befinden sich im folgenden Registrierungsschlüssel:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

Im folgenden werden die WFP-Registrierungs Werte angezeigt.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

Speicherort des Caches. Dies muss ein lokaler Pfad sein. Der Standardwert ist% SystemRoot% \\ system32 \\ Dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Kontingent Optionen. Bei diesem Registrierungs Wert kann es sich um einen der folgenden Werte handeln:



| Wert                  | Bedeutung                                                  |
|------------------------|----------------------------------------------------------|
| SFC- \_ Kontingent für \_ alle \_ Dateien | Die Größe des dll-Caches ist unbegrenzt. Dies ist die Standardoption. |
| Andere Werte           | Größe des dll-Caches in Dateien.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SfcScan**
</dt> <dd>

Überprüfungs Optionen. Bei diesem Registrierungs Wert kann es sich um einen der folgenden Werte handeln:



| Wert             | Bedeutung                                                   |
|-------------------|-----------------------------------------------------------|
| SFC- \_ Scan \_ Normal | Überprüfen Sie keine geschützten Dateien beim Start. Dies ist die Standardoption. |
| SFC- \_ Scan \_ immer | Überprüfen geschützter Dateien bei jedem Start.                       |
| SFC- \_ Scan einmalig \_   | Überprüfen geschützter Dateien beim nächsten Start.                    |



 

</dd> </dl>

 

 



