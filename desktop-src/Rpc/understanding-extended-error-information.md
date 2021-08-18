---
title: Grundlegendes zu erweiterten Fehlerinformationen
description: Erweiterte Fehlerinformationen sind ein Array von Datensätzen, die jeweils die Übergabe des Fehlercodes über eine bestimmte Ebene im System oder in der Anwendung angeben.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e003214198b06f04479ec4c1a8d23cb1acedafda49eefcf2880741416901323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011058"
---
# <a name="understanding-extended-error-information"></a>Grundlegendes zu erweiterten Fehlerinformationen

Erweiterte Fehlerinformationen sind ein Array von Datensätzen, die jeweils die Übergabe des Fehlercodes über eine bestimmte Ebene im System oder in der Anwendung angeben. Wenn ein Fehler auf Computer C auftritt, wie er von Computer B aufgerufen wird, der wiederum von Computer A aufgerufen wird, generiert die RPC-Laufzeit auf Computer C einen oder mehrere Datensätze, die den Fehler beschreiben, und übergibt sie an Computer B. Computer B kann dem Kopf der vorhandenen Kette einen oder mehrere Datensätze hinzufügen.  und übergibt die vollständige Kette an A. Kann einen oder mehrere Datensätze hinzufügen und die Informationen anzeigen oder protokollieren. Im Wesentlichen stellt die erweiterte Fehlerkette den Verlauf des Fehlers dar.

Erweiterte Fehlerinformationen ersetzen nicht den Fehlercode \_ (rpc-S-Statuscode). \_ \* Unabhängig davon, wie viele oder ob erweiterte Fehlerinformationen generiert werden, bleibt der Fehlercode unverändert.

Jeder erweiterte Fehlerinformationsdatensatz enthält Folgendes. Weitere Informationen finden Sie unter [**RPC EXTENDED ERROR INFO (RPC EXTENDED ERROR \_ \_ \_ INFO):**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)

-   ComputerName: Dies ist der nicht qualifizierte DNS-Name des Computers, auf dem der Fehler aufgetreten ist. Nur Datensätze an Computergrenzen verfügen über diese Informationen. In dem zuvor beschriebenen Szenario mit den Computern A, B und C wird computerName beispielsweise für die folgenden Felder definiert:

    | Datensatz                            | Feld "ComputerName" |
    |-----------------------------------|--------------------|
    | Datensatz \# 1, der von Computer C generiert wurde | \-                 |
    | Von Computer C generierter Datensatz \# 2 | \-                 |
    | Von Computer C generierter Datensatz \# 3 | C                  |
    | Datensatz \# 1, der von Computer B generiert wurde | \-                 |
    | Von Computer B generierter Datensatz \# 2 | \-                 |
    | Von Computer B generierter Datensatz \# 3 | B                  |
    | Datensatz \# 1, der von Computer A generiert wurde | \-                 |
    | Datensatz \# 2, der von Computer A generiert wurde | \-                 |
    | Von Computer A generierter Datensatz \# 3 | \-                 |
    | Kopf der Kette                 |                    |

    

     

<!-- -->

-   ProcessID: Prozessbezeichner des Prozesses, der den Fehler generiert hat.
-   TimeStamp– Zeitpunkt, zu dem der Fehler aufgetreten ist, ausgedrückt im UTC-Format.
-   Generieren einer Komponente : Ganzzahlige Codedefinition der logischen Komponente, die den Fehler generiert hat. Die folgenden Komponenten sind derzeit definiert:

    | Code | Name              | Beschreibung                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Anwendung       | Die Komponente, die die Managerroutine für den jeweiligen RPC-Aufruf besitzt                                                                                                                  |
    | 2    | Typ           | Die RPC-Laufzeit                                                                                                                                                                      |
    | 3    | Sicherheitsanbieter | Der Sicherheitsanbieter für diesen Aufruf.                                                                                                                                                  |
    | 4    | Npfs              | Das NPFS-Dateisystem                                                                                                                                                                  |
    | 5    | Rdr               | Der Redirector                                                                                                                                                                        |
    | 6    | Nmp               | Das Named Pipe-System. Dies kann entweder NPFS oder RDR sein, aber in vielen Fällen weiß die RPC-Laufzeit nicht, wer den angeforderten Vorgang ausgeführt hat, und in solchen Fällen wird NMP zurückgegeben. |
    | 7    | IO                | Das E/A-System oder ein vom E/A-System verwendeter Treiber. Dies kann entweder NPFS, RDR oder ein Winsock-Anbieter sein.                                                                                 |
    | 8    | Winsock           | Der Winsock-Anbieter                                                                                                                                                                  |
    | 9    | Authz-Code        | Die Autorisierungs-APIs.                                                                                                                                                               |
    | 10   | Lpc               | Die Funktion Lokaler Prozeduraufruf.                                                                                                                                                    |

    

     

<!-- -->

-   Status : Fehlercode, der von der Ebene generiert oder zurückgegeben wird
-   DetectionLocation: eindeutige Nummer, die den Speicherort des Codes identifiziert, an dem der Fehler erkannt wurde. Dieses Feld ist an den Code gebunden und ändert sich von Version zu Version. Eine separate Liste der am häufigsten gefundenen Erkennungsspeicherorte wird veröffentlicht.
-   Flags: Flags, die Informationen zum Datensatz angeben. Die derzeit definierten Flags sind EEInfoPreviousRecordsMissing und EEInfoNextRecordsMissing, die den numerischen Werten 1 bzw. 2 entsprechen. Wenn EEInfoPreviousRecordsMissing festgelegt ist, fehlen mindestens ein Datensatz vor diesem Datensatz. Wenn EEInfoNextRecordsMissing festgelegt ist, fehlen mindestens ein Datensatz nach diesem Datensatz. Eine Beschreibung, warum Datensätze möglicherweise fehlen, finden Sie unter [Zuverlässigkeit erweiterter Fehlerinformationen.](reliability-of-extended-error-information.md)
-   Bis zu vier Fehlerparameter. Ein Fehlerparameter ist eine einfache Variant-Struktur, die zusätzliche Informationen zum Fehler bereitstellt. Die zusätzlichen Informationen hängen vom Fehler und dem Erkennungsspeicherort ab. Die Parameter können vom Typ ANSI String (LPSTR), Unicode String (LPWSTR), long value (long), short value (short), pointer (int64) oder none sein.

 

 




