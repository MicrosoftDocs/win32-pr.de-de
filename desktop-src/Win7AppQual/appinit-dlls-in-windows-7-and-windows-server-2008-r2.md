---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363415"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>AppInit \_ -DLLs in Windows 7 und Windows Server 2008 R2

## <a name="platform"></a>Plattform

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Bei AppInit- \_ DLLs handelt es sich um einen Mechanismus, mit dem eine beliebige Liste von DLLs in jeden Benutzermodusprozess auf dem System geladen werden kann. Microsoft ändert die AppInit-DLLs-Funktion in Windows 7 und Windows Server 2008 R2, um eine neue Code Signatur Anforderung hinzuzufügen. Dadurch wird die Zuverlässigkeit und Leistung des Systems verbessert, und der Einblick in den Ursprung der Software wird verbessert.

## <a name="configuration"></a>Konfiguration

Werte, die unter der HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows Key in der Registrierung gespeichert sind, bestimmen das Verhalten der AppInit- \_ DLLs-Infrastruktur. In der folgenden Tabelle werden diese Registrierungs Werte beschrieben:



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
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {Remove} $<br />
</td>
<td rowspan="2">Hiermit werden AppInit_DLLs. $ {Remove} $ global aktiviert oder deaktiviert.<br />
</td>
<td>0x0 – AppInit_DLLs sind deaktiviert.</td>
</tr>
<tr class="even">
<td>0x1 – AppInit_DLLs aktiviert sind.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Durch Trennzeichen getrennte Liste der zu ladenden DLLs. Der gesamte Pfad zur DLL sollte mithilfe von Kurznamen angegeben werden.</td>
<td>C:\ PROGRA ~ 1 \ WID288 ~ 1 \ Micros ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {Remove} $<br />
</td>
<td rowspan="2">Nur Code signierte DLLs laden. $ {Remove} $<br />
</td>
<td>0x0 – laden Sie alle DLLs.</td>
</tr>
<tr class="odd">
<td>0x1 – nur Code signierte DLLs laden.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Alle DLLs, die von der AppInit- \_ DLLs-Infrastruktur geladen werden, sollten Code signiert sein. Im Interesse der Anwendungs Kompatibilität lädt das Windows 7-Betriebs System alle AppInit-DLLs. Microsoft empfiehlt jedoch, dass alle Anwendungsentwickler ihre DLLs Code signieren, um die Zuverlässigkeit von Windows zu verbessern und die Code Signatur in zukünftigen Versionen von Windows vorzubereiten. Der Registrierungsschlüssel "Requirements signetdappinit \_ DLLs" steuert dieses Verhalten, und sein Wert unter Windows 7 ist standardmäßig auf 0 festgelegt.

**Windows Server 2008 R2**

Alle DLLs, die von der AppInit- \_ DLLs-Infrastruktur geladen werden, müssen Code signiert sein. Der Registrierungsschlüssel "Requirements signetdappinit \_ DLLs" steuert dieses Verhalten, und sein Wert unter Windows Server 2008 R2 ist standardmäßig auf 1 festgelegt.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[AppInit-DLLs in Windows 7 und Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
