---
title: Managed Reference for BITS PowerShell Commands
description: In Background Intelligent Transfer Service (Bits) 4,0 können Windows PowerShell-Cmdlets zum Verwalten von Übertragungs Aufträgen verwendet werden.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858369"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Managed Reference for BITS PowerShell Commands

In Background Intelligent Transfer Service (Bits) 4,0 können Windows PowerShell-Cmdlets zum Erstellen und Verwalten von Dateidownloads und Hochladen von Übertragungs Aufträgen verwendet werden.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

Windows PowerShell-Cmdlets für Bits bieten einen Großteil der gleichen Funktionen wie das BITSAdmin-Befehlszeilenprogramm. Windows PowerShell führt jedoch auch die folgenden Schritte aus:

-   Automatisiert Bits-Aufgaben in einer erweiterbaren und Verwaltungs orientierten Skriptsprache.
-   Stellt ein einzelnes Tool für alle auftragsbezogenen Aufgaben bereit.

> [!Note]  
> Um diese Befehle verwenden zu können, müssen Sie zunächst das Bits-PowerShell-Modul mit dem `Import-Module BitsTransfer` Befehl importieren. Weitere Informationen finden Sie im folgenden [TechNet-Artikel](/previous-versions/technet-magazine/ff382721(v=msdn.10)).

 

Weitere Informationen zur Verwendung von Windows PowerShell finden Sie unter [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>Bits-PowerShell-Klassen

**Namespace**: Microsoft. backgroundintelligenttransfer. Management

**Assembly**: System. Management. Automation

Diese Bits-Befehls Klassen werden von Windows PowerShell implementiert. Diese Klassen sind nur aus Gründen der Vollständigkeit in diesem Software Development Kit (SDK) enthalten. Die Member dieser Klassen können nicht direkt verwendet werden und sollten nicht zum Ableiten anderer Klassen verwendet werden.



| Klasse                           | BESCHREIBUNG                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Addbihandfilecommand**          | Fügt einem vorhandenen Bits-Übertragungs Auftrag eine oder mehrere Dateien hinzu.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet " [Add-bizfile](/previous-versions//dd347701(v=technet.10)) ".<br/>                       |
| **Clearbitstransfercommand**    | Bricht einen Bits-Übertragungs Auftrag ab.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet " [Clear-bitstransfer]( /previous-versions//dd347701(v=technet.10)) ".<br/>                                          |
| **Completebitstransfercommand** | Schließt einen Bits-Übertragungs Auftrag ab.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet [Complete-bitstransfer]( /previous-versions//dd347701(v=technet.10)) .<br/>                                     |
| **Getbitstransfercommand**      | Ruft das zugeordnete bitsjob-Objekt für einen vorhandenen Bits-Übertragungs Auftrag ab.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet " [Get-bitstransfer](/previous-versions//dd347701(v=technet.10)) ".<br/> |
| **Newbitstransfercommand**      | Erstellt einen neuen Bits-Übertragungs Auftrag.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet [New-bitstransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                           |
| **Resumebitstransfercommand**   | Setzt einen Bits-Übertragungs Auftrag fort.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet [Resume-bitstransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                            |
| **Setbitstransfercommand**      | Ändert die Eigenschaften eines vorhandenen Bits-Übertragungs Auftrags.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet [Set-bitstransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                  |
| **Suspendbitstransfercommand**  | Hält einen Bits-Übertragungs Auftrag an.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet [Suspend-bitstransfer](/previous-versions//dd347701(v=technet.10)) .<br/>                                          |



 

 

