---
title: Managed Reference for BITS PowerShell Commands
description: Background Intelligent Transfer Service (BITS) 4.0 können Windows PowerShell Cmdlets verwenden, um Übertragungsaufträge zu verwalten.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc88c557209ed2958d06766215278e75223a1b297bd2704ca1dcba062cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173856"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Managed Reference for BITS PowerShell Commands

Background Intelligent Transfer Service (BITS) 4.0 kann Windows PowerShell Cmdlets verwenden, um Dateidownload- und Uploadübertragungsaufträge zu erstellen und zu verwalten.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

Windows PowerShell Cmdlets für BITS bieten einen Großteil der gleichen Funktionalität wie das Befehlszeilenprogramm bitsadmin. Windows PowerShell führt jedoch auch folgende Schritte aus:

-   Automatisiert BITS-Aufgaben in einer erweiterbaren und verwaltungsorientierten Skriptsprache.
-   Stellt ein einzelnes Tool für alle auftragsbezogenen Aufgaben bereit.

> [!Note]  
> Um diese Befehle verwenden zu können, müssen Sie zunächst das BITS PowerShell-Modul importieren, indem Sie den `Import-Module BitsTransfer` Befehl verwenden. Weitere Informationen finden Sie im [techNet-Artikel](/previous-versions/technet-magazine/ff382721(v=msdn.10)).

 

Weitere Informationen zur Verwendung von Windows PowerShell finden Sie unter [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>BITS-PowerShell-Klassen

**Namespace:** Microsoft.BackgroundIntelligentTransfer.Management

**Assembly:** System.Management.Automation

Diese BITS-Befehlsklassen werden von Windows PowerShell implementiert. Diese Klassen sind nur zur Vollständigkeit in diesem Software Development Kit (SDK) enthalten. Die Member dieser Klassen können weder direkt noch zum Ableiten anderer Klassen verwendet werden.



| Klasse                           | Beschreibung                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | Fügt einem vorhandenen BITS-Übertragungsauftrag eine oder mehrere Dateien hinzu.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [Add-BitsFile.](/previous-versions//dd347701(v=technet.10))<br/>                       |
| **ClearBitsTransferCommand**    | Bricht einen BITS-Übertragungsauftrag ab.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im [Cmdlet Clear-BitsTransfer.]( /previous-versions//dd347701(v=technet.10))<br/>                                          |
| **CompleteBitsTransferCommand** | Schließt einen BITS-Übertragungsauftrag ab.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im [Complete-BitsTransfer-Cmdlet.]( /previous-versions//dd347701(v=technet.10))<br/>                                     |
| **GetBitsTransferCommand**      | Ruft das zugeordnete BitsJob-Objekt für einen vorhandenen BITS-Übertragungsauftrag ab.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [Get-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/> |
| **NewBitsTransferCommand**      | Erstellt einen neuen BITS-Übertragungsauftrag.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [New-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/>                                           |
| **ResumeBitsTransferCommand**   | Setzt einen BITS-Übertragungsauftrag fort.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [Resume-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/>                                            |
| **SetBitsTransferCommand**      | Ändert die Eigenschaften eines vorhandenen BITS-Übertragungsauftrags.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [Set-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/>                  |
| **SuspendBitsTransferCommand**  | Unterbricht einen BITS-Übertragungsauftrag.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [Suspend-BitsTransfer.](/previous-versions//dd347701(v=technet.10))<br/>                                          |



 

 

