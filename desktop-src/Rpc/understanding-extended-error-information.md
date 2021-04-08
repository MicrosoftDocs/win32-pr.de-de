---
title: Grundlegendes zu erweiterten Fehlerinformationen
description: Erweiterte Fehlerinformationen sind ein Array von Datensätzen, die jeweils angeben, dass der Fehlercode durch eine bestimmte Ebene im System oder in der Anwendung übergeben wird.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2918caa446f7cee9c4eaa609a5713c9cb385e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037323"
---
# <a name="understanding-extended-error-information"></a>Grundlegendes zu erweiterten Fehlerinformationen

Erweiterte Fehlerinformationen sind ein Array von Datensätzen, die jeweils angeben, dass der Fehlercode durch eine bestimmte Ebene im System oder in der Anwendung übergeben wird. Wenn ein Fehler auf einem Computer c auftritt, während er von Computer b aufgerufen wird, der wiederum von Computer a aufgerufen wird, generiert die RPC-Laufzeit auf Computer c mindestens einen Datensatz, der den Fehler beschreibt, und übergibt sie an den Computer b. Computer B kann dem Anfang der vorhandenen Kette einen oder mehrere Datensätze hinzufügen und übergibt die vollständige Kette an eine. Ein kann einen oder mehrere Datensätze hinzufügen und die Informationen anzeigen oder protokollieren. Im Grunde stellt die erweiterte Fehlerkette den Verlauf des Fehlers dar.

Erweiterte Fehlerinformationen ersetzen nicht den Fehlercode (den RPC \_ S- \_ \* Statuscode). Unabhängig davon, wie viel oder ob erweiterte Fehlerinformationen generiert werden, bleibt der Fehlercode unverändert.

Jeder Datensatz für erweiterte Fehlerinformationen enthält Folgendes: Weitere Informationen finden Sie in der [**erweiterten RPC- \_ \_ Fehler \_ Info**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) :

-   Computername – Dies ist der nicht qualifizierte DNS-Name des Computers, von dem der Fehler verursacht wurde. Nur Datensätze in den Computer Grenzen verfügen über diese Informationen. Beispielsweise wird in dem zuvor beschriebenen Szenario mit den Computern A, B und C der Computername für die folgenden Felder definiert:

    | Datensatz                            | Feld "Computername" |
    |-----------------------------------|--------------------|
    | Datensatz \# 1 von Computer C generiert | \-                 |
    | Datensatz \# 2 von Computer C generiert | \-                 |
    | Datensatz \# 3 generiert von Computer C | C                  |
    | Datensatz \# 1 generiert von Computer B | \-                 |
    | Datensatz \# 2 generiert von Computer B | \-                 |
    | Datensatz \# 3 generiert von Computer B | B                  |
    | Datensatz \# 1 generiert von Computer A | \-                 |
    | Datensatz \# 2 generiert von Computer A | \-                 |
    | Datensatz \# 3 generiert von Computer A | \-                 |
    | Anfang der Kette                 |                    |

    

     

<!-- -->

-   ProcessID – Prozess-ID des Prozesses, der den Fehler generiert hat.
-   Zeitstempel – Zeit, zu der der Fehler aufgetreten ist, ausgedrückt im UTC-Format.
-   Generieren der Komponente – ganzzahlige Code Definition der logischen Komponente, die den Fehler generiert hat. Die folgenden Komponenten sind aktuell definiert:

    | Code | Name              | BESCHREIBUNG                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Application       | Die Komponente, die die Manager-Routine für den jeweiligen RPC-Aufruf besitzt.                                                                                                                  |
    | 2    | Typ           | Die RPC-Laufzeit                                                                                                                                                                      |
    | 3    | Sicherheitsanbieter | Der Sicherheitsanbieter für diesen-Befehl.                                                                                                                                                  |
    | 4    | NPFS              | Das NPFS-Dateisystem                                                                                                                                                                  |
    | 5    | RDR               | Der Redirector                                                                                                                                                                        |
    | 6    | NMP               | Das Named Pipe System. Dabei kann es sich entweder um NPFS oder um RDR handeln, aber in vielen Fällen weiß die RPC-Laufzeit nicht, wer den angeforderten Vorgang ausgeführt hat, und in solchen Fällen wird NMP zurückgegeben. |
    | 7    | IO                | Das e/a-System oder ein vom IO-System verwendeter Treiber. Dies kann entweder NPFS, rdr oder ein Winsock-Anbieter sein.                                                                                 |
    | 8    | Winsock           | Der Winsock-Anbieter                                                                                                                                                                  |
    | 9    | Authz-Code        | Die Autorisierungs-APIs.                                                                                                                                                               |
    | 10   | LPC               | Die Einrichtung des lokalen Prozedur Aufrufes.                                                                                                                                                    |

    

     

<!-- -->

-   Status – Fehlercode, der von der Ebene generiert oder zurückgegeben wird
-   Detectionlocation – eindeutige Nummer, die den Speicherort des Codes identifiziert, in dem der Fehler erkannt wurde. Dieses Feld ist mit dem Code verknüpft und wechselt von Version zu Version. Eine separate Liste der am häufigsten gefundenen Erkennungs Speicherorte wird veröffentlicht.
-   Flags – Flags, die Informationen über den Datensatz angeben. Die zurzeit definierten Flags sind eeingefopreviousrecordsmissing und EEin fonextrecordsmissing, die den numerischen Werten 1 und 2 entsprechen. Wenn eeinf opreviousrecordsmissing festgelegt ist, fehlt ein oder mehrere Datensätze vor dem Datensatz. Wenn eeinfonextrecordsmissing festgelegt ist, fehlt ein oder mehrere Datensätze nach dem Datensatz. Informationen dazu, warum Datensätze möglicherweise fehlen, finden Sie unter [Zuverlässigkeit erweiterter Fehlerinformationen](reliability-of-extended-error-information.md).
-   Bis zu vier Fehler Parameter. Ein Fehler Parameter ist eine vereinfachte VARIANT-Struktur, die zusätzliche Informationen über den Fehler bereitstellt. Die zusätzlichen Informationen hängen von dem Fehler und dem Erkennungs Speicherort ab. Die Parameter können den Typ "ANSI String (LPSTR)", "Unicode String (LPWSTR)", "Long Value (Long)", "Short Value (Short)", "Pointer" (Int64) oder "None" aufweisen.

 

 




