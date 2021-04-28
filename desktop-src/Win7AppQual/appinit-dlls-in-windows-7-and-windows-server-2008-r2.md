---
description: AppInit_DLLs in Windows 7 und Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs unter Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088708"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>\_AppInit-DLLs in Windows 7 und Windows Server 2008 R2

## <a name="platform"></a>Plattform

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Niedrig  





## <a name="description"></a>BESCHREIBUNG

AppInit-DLLs sind ein Mechanismus, mit dem eine beliebige Liste von DLLs in jeden Benutzermodusprozess im \_ System geladen werden kann. Microsoft ändert die AppInit-DLLs in Windows 7 und Windows Server 2008 R2, um eine neue Codesignaturanforderung hinzuzufügen. Dies hilft, die Zuverlässigkeit und Leistung des Systems zu verbessern und den Einblick in den Ursprung der Software zu verbessern.

## <a name="configuration"></a>Konfiguration

Werte, die unter dem Windows-Schlüssel HKEY LOCAL MACHINE SOFTWARE Microsoft Windows NT CurrentVersion In der Registrierung gespeichert sind, bestimmen das Verhalten der \_ \_ \\ \\ \\ \\ \\ AppInit-DLLs-Infrastruktur. \_ In der folgenden Tabelle werden diese Registrierungswerte beschrieben:



<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
<th>Beispielwerte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$<br />
</td>
<td rowspan="2">Aktiviert oder deaktiviert global AppInit_DLLs.${REMOVE}$<br />
</td>
<td>0x0 : AppInit_DLLs sind deaktiviert.</td>
</tr>
<tr class="even">
<td>0x1 : AppInit_DLLs sind aktiviert.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Durch Leerzeichen oder Kommas getrennte Liste der zu ladenden DLLs. Der vollständige Pfad zur DLL sollte mithilfe von Kurznamen angegeben werden.</td>
<td>C:\ PROGRA~1\WID288~1\MICROS~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$<br />
</td>
<td rowspan="2">Nur mit Code signierte DLLs laden.${REMOVE}$<br />
</td>
<td>0x0: Alle DLLs werden geladen.</td>
</tr>
<tr class="odd">
<td>0x1: Lädt nur mit Code signierte DLLs.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Alle DLLs, die von der \_ AppInit-DLLs-Infrastruktur geladen werden, sollten mit Code signiert sein. Aus Gründen der Anwendungskompatibilität lädt das Windows 7-Betriebssystem alle AppInit-DLLs. Microsoft empfiehlt jedoch, dass alle Anwendungsentwickler ihre DLLs codesignieren, um die Zuverlässigkeit von Windows zu verbessern und die Codesignaturerzwingung in zukünftigen Versionen von Windows vorzubereiten. Der Registrierungsschlüssel RequireSignedAppInit \_ DLLs steuert dieses Verhalten, und sein Wert unter Windows 7 ist standardmäßig auf 0 festgelegt.

**Windows Server 2008 R2**

Alle DLLs, die von der \_ AppInit-DLLs-Infrastruktur geladen werden, müssen mit Code signiert sein. Der Registrierungsschlüssel RequireSignedAppInit \_ DLLs steuert dieses Verhalten, und sein Wert unter Windows Server 2008 R2 ist standardmäßig auf 1 festgelegt.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[AppInit-DLLs unter Windows 7 und Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
