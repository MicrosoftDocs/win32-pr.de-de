---
description: Streamkontexte verarbeiten die sicheren Datenstrom orientierten Protokolle, wie z. b. SSL oder PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Streamkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53103dc1269c05e5a2c162133d21e167d8035c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959348"
---
# <a name="stream-contexts"></a>Streamkontexte

Streamkontexte verarbeiten die sicheren Datenstrom orientierten Protokolle, wie z. b. SSL oder PCT. Um die gleiche Schnittstelle und ähnliche Verwaltung von Anmelde Informationen zu nutzen, bietet SSPI Unterstützung für streamkontexte. Das [*Sicherheitsprotokoll*](../secgloss/s-gly.md) enthält sowohl das streamingauthentifizierungsschema als auch Datensatzformate.

Zum Bereitstellen von streamorientierten Protokollen weisen [*Sicherheitspakete*](../secgloss/s-gly.md) , die streamkontexte unterstützen, die folgenden Prozess Eigenschaften auf:

-   Das Paket legt das Flag "secpkg Flag Stream" fest, \_ \_ um anzugeben, dass die Datenstrom Semantik unterstützt wird.
-   Transport Anwendungen fordern eine Datenstrom Semantik an, indem Sie die Funktionen "ISC \_ req \_ Stream" und "ASC \_ req \_ Stream" in den Aufrufen der Funktionen " [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) " und " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " festlegen.
-   Die Anwendung ruft die [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) -Funktion mit einer [**secpkgcontext \_ streamsizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) -Struktur auf, um den [*Sicherheitskontext*](../secgloss/s-gly.md) für die Anzahl der bereit zustellenden Puffer und die für Header oder Nachspann zu reservierenden Größen abzufragen.
-   Die Anwendung bietet Puffer Deskriptoren, die während der eigentlichen Verarbeitung der Daten verschont werden. Durch die Angabe der Datenstrom Semantik weist der Aufrufer die Bereitschaft an, zusätzliche Verarbeitungsschritte durchzuführen, damit das [*Sicherheitspaket*](../secgloss/s-gly.md) die Blockierung der Nachrichten verarbeiten kann. Im wesentlichen übergibt der Aufrufer für die Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) eine Liste der Puffer. Wenn eine Nachricht von einem Stream-orientierten Kanal empfangen wird (z. b. einem TCP-Port), übergibt der Aufrufer wie folgt eine Puffer Liste.

    | Buffer | Länge         | Puffertyp      |
    |--------|----------------|------------------|
    | 1      | Nachrichten Länge | secbuffer- \_ Daten  |
    | 2      | 0              | secbuffer ist \_ leer. |
    | 3      | 0              | secbuffer ist \_ leer. |
    | 4      | 0              | secbuffer ist \_ leer. |
    | 5      | 0              | secbuffer ist \_ leer. |

    

     

    Das Sicherheitspaket funktioniert dann für das [*BLOB*](../secgloss/b-gly.md). Wenn die Funktion erfolgreich zurückgegeben wird, sieht die Puffer Liste wie folgt aus.

    

    | Buffer | Länge         | Puffertyp                |
    |--------|----------------|----------------------------|
    | 1      | Header Länge  | secbuffer \_ - \_ Streamheader  |
    | 2      | Daten Länge    | secbuffer- \_ Daten            |
    | 3      | Nachspann Länge | secbuffer- \_ streamnachspann \_ |
    | 4      | 0              | secbuffer ist \_ leer.           |
    | 5      | 0              | secbuffer ist \_ leer.           |

    

     

    Das Paket könnte auch Puffer \# 4 mit der Länge x und den Puffertyp secbuffer extra zurückgegeben haben \_ , um anzugeben, dass die Daten in diesem Puffer Teil des nächsten Datensatzes sind und noch nicht verarbeitet wurden. Wenn die Message-Funktion hingegen den \_ \_ Fehlercode der unvollständigen Sek.-Nachricht zurückgibt \_ , würde die zurückgegebene Puffer Liste wie folgt aussehen.

    

    | Buffer | Länge | Puffertyp        |
    |--------|--------|--------------------|
    | 1      | x      | secbuffer \_ fehlt. |

    

     

    Dies weist darauf hin, dass für die Verarbeitung des Datensatzes mehr Daten benötigt wurden. Im Gegensatz zu den meisten von einer Nachrichten Funktion zurückgegebenen Fehlern zeigt dieser Puffertyp nicht an, dass der Kontext kompromittiert wurde. Stattdessen wird angegeben, dass mehr Daten benötigt werden. [*Sicherheitspakete*](../secgloss/s-gly.md) dürfen Ihren [*Status*](../secgloss/s-gly.md) in diesem Zustand nicht aktualisieren.

    Ebenso kann der Aufrufer auf der Absender Seite der Kommunikation die [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion aufzurufen. Das Sicherheitspaket muss den Puffer möglicherweise erneut zuordnen oder die Dinge kopieren. Der Aufrufer kann effizienter sein, indem er wie folgt eine Puffer Liste bereitstellt.

    

    | Buffer | Länge         | type                       |
    |--------|----------------|----------------------------|
    | 1      | Header Länge  | secbuffer \_ - \_ Streamheader  |
    | 2      | Daten Länge    | secbuffer- \_ Daten            |
    | 3      | Nachspann Länge | secbuffer- \_ streamnachspann \_ |

    

     

    Dies ermöglicht es dem Aufrufer, die Puffer effizienter zu verwenden. Durch Aufrufen der [**QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) -Funktion zum Ermitteln des Speicherplatzes, der reserviert werden soll, bevor [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)aufgerufen wird, ist der Vorgang für die Anwendung und das Sicherheitspaket effizienter.

 

 
