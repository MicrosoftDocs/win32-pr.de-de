---
description: Streamkontexte verarbeiten die sicheren streamorientierten Protokolle wie SSL oder PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Streamkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c843889df6aec3f82e8cb8516a7c23ccbf7a6de9957f9a0c572f6e6ca63ac75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916679"
---
# <a name="stream-contexts"></a>Streamkontexte

Streamkontexte verarbeiten die sicheren streamorientierten Protokolle wie SSL oder PCT. Im Interesse der gemeinsamen Nutzung derselben Schnittstelle und ähnlicher Verwaltung von Anmeldeinformationen bietet SSPI Unterstützung für Streamkontexte. Das [*Sicherheitsprotokoll umfasst*](../secgloss/s-gly.md) sowohl das Streamauthentifizierungsschema als auch die Datensatzformate.

Sicherheitspakete, die Streamkontexte [*unterstützen,*](../secgloss/s-gly.md) verfügen über die folgenden Prozessmerkmale, um streamorientierte Protokolle bereitstellen zu können:

-   Das Paket legt das FLAG SECPKG \_ FLAG \_ STREAM fest, um anzugeben, dass es Streamsemantik unterstützt.
-   Transportanwendungen fordern Streamsemantik an, indem sie die ISC \_ REQ STREAM- und ASC REQ STREAM-Flags in den Aufrufen der \_ Funktionen \_ \_ [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) und [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) festlegen.
-   Die Anwendung ruft die [**QueryContextAttributes (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) mit einer [**SecPkgContext \_ StreamSizes-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) auf, um den Sicherheitskontext nach der Anzahl der bereitgestellten Puffer und den größen zu reservierenden Größen für Header oder Nachspannen abfragt. [](../secgloss/s-gly.md)
-   Die Anwendung bietet Pufferdeskriptoren, die während der eigentlichen Verarbeitung der Daten verschont werden müssen. Durch Angabe der Streamsemantik gibt der Aufrufer die [](../secgloss/s-gly.md) Bereitschaft an, zusätzliche Verarbeitungen zu übernehmen, damit das Sicherheitspaket die Blockierung der Nachrichten verarbeiten kann. Im Wesentlichen übergibt der Aufrufer für die [**Funktionen MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) eine Liste von Puffern. Wenn eine Nachricht von einem streamorientierten Kanal (z. B. einem TCP-Port) empfangen wird, übergibt der Aufrufer wie folgt eine Pufferliste.

    | Buffer | Länge         | Puffertyp      |
    |--------|----------------|------------------|
    | 1      | Nachrichtenlänge | \_SECBUFFER-DATEN  |
    | 2      | 0              | SECBUFFER \_ EMPTY |
    | 3      | 0              | SECBUFFER \_ EMPTY |
    | 4      | 0              | SECBUFFER \_ EMPTY |
    | 5      | 0              | SECBUFFER \_ EMPTY |

    

     

    Das Sicherheitspaket funktioniert dann im [*BLOB*](../secgloss/b-gly.md). Wenn die Funktion erfolgreich zurückgegeben wird, sieht die Pufferliste wie folgt aus.

    

    | Buffer | Länge         | Puffertyp                |
    |--------|----------------|----------------------------|
    | 1      | Headerlänge  | \_SECBUFFER-STREAMHEADER \_  |
    | 2      | Datenlänge    | \_SECBUFFER-DATEN            |
    | 3      | Länge des Nachspanns | SECBUFFER \_ STREAM \_ TRAILER |
    | 4      | 0              | SECBUFFER \_ EMPTY           |
    | 5      | 0              | SECBUFFER \_ EMPTY           |

    

     

    Das Paket hätte auch den Puffer 4 mit der Länge x und dem Puffertyp SECBUFFER EXTRA zurückgegeben, der angibt, dass die Daten in diesem Puffer Teil des nächsten Datensatzes sind und noch \# \_ nicht verarbeitet wurden. Wenn die Nachrichtenfunktion umgekehrt den Fehlercode SEC E INCOMPLETE MESSAGE zurückgibt, sieht die zurückgegebene Pufferliste \_ \_ wie folgt \_ aus.

    

    | Buffer | Länge | Puffertyp        |
    |--------|--------|--------------------|
    | 1      | x      | SECBUFFER \_ FEHLT |

    

     

    Dies weist darauf hin, dass weitere Daten zum Verarbeiten des Datensatzes erforderlich waren. Im Gegensatz zu den meisten Fehlern, die von einer Nachrichtenfunktion zurückgegeben werden, gibt dieser Puffertyp nicht an, dass der Kontext kompromittiert wurde. Stattdessen gibt sie an, dass mehr Daten benötigt werden. [*-Sicherheitspakete*](../secgloss/s-gly.md) dürfen ihren Zustand in [*dieser*](../secgloss/s-gly.md) Bedingung nicht aktualisieren.

    Auf ähnliche Weise kann der Aufrufer auf absenderseitiger Seite der Kommunikation die [**MakeSignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-makesignature) aufrufen. Das Sicherheitspaket muss möglicherweise den Puffer neu zuspeichern oder Dinge kopieren. Der Aufrufer kann effizienter sein, indem er eine Pufferliste wie folgt an die Hand gibt.

    

    | Buffer | Länge         | type                       |
    |--------|----------------|----------------------------|
    | 1      | Headerlänge  | \_SECBUFFER-STREAMHEADER \_  |
    | 2      | Datenlänge    | \_SECBUFFER-DATEN            |
    | 3      | Länge des Nachspanns | SECBUFFER \_ STREAM \_ TRAILER |

    

     

    Dadurch kann der Aufrufer die Puffer effizienter verwenden. Durch Aufrufen der [**QueryContextAttributes-Funktion,**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) um den zu reservierenden Speicherplatz vor dem Aufruf von [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)zu bestimmen, ist der Vorgang für die Anwendung und das Sicherheitspaket effizienter.

 

 
