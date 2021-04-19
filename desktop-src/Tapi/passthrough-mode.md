---
description: Wenn ein-Befehl in der Passthrough-Anleitung von linebearermode aktiv ist \_ , ermöglicht der Dienstanbieter den direkten Zugriff auf die angefügte Hardware, die von der Anwendung gesteuert werden kann.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Passthrough-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985e1caf666fcb3278bacf5c5cfe9d8a4e847dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353152"
---
# <a name="passthrough-mode"></a>Passthrough-Modus

Wenn ein-Befehl in der **\_ Passthrough-Anleitung von linebearermode** aktiv ist, ermöglicht der Dienstanbieter den direkten Zugriff auf die angefügte Hardware, die von der Anwendung gesteuert werden kann. Anwendungen können diesen Modus für die temporäre direkte Steuerung von asynchronen Modems verwenden, auf die über die [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zugegriffen wird, um spezielle Features zu konfigurieren oder zu verwenden, die andernfalls vom Dienstanbieter nicht unterstützt werden (z. b. für das Fax (Class 1, 2 usw.). Dieser bearermodus wird vom Dienstanbieter für universelle Modemtreiber (Unimodem) unterstützt.

Dienstanbieter, die die **\_ Passthrough-Angabe linebearermode** unterstützen, geben diese im **dwbearermodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur an. Wenn die Passthrough-Angabe für **linebearermode \_** angegeben ist, enthält der Unimodem-Dienstanbieter auch im folgenden Format  den Registrierungsschlüssel, der **für den Zugriff** auf Daten über das mit dem liniengerät verknüpfte Modem verwendet wird:

``` syntax
struct {
    DWORD dwContents;   // Set to 1 (indicates containing key).
    DWORD dwKeyOffset;  // Offset to key from start of this
                        // structure (not from start of
                        // LINEDEVCAPS structure).
                        // 8 in this case. 
    BYTE rgby[...];     // Place that contains null-terminated
                        // registry key. 
}
```

Beispiel:

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

Dieser Registrierungsschlüssel kann dann mithilfe der [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) -Funktion geöffnet werden.

Der Pass-Through-Modus wird am häufigsten mit der [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) -Funktion aufgerufen, indem das **linebearermode- \_ Passthrough** -Bit im **dwbearermode** -Member der [**linecallbiams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur festgelegt wird, auf die durch den *lpcallparser* -Parameter verwiesen wird. Wenn dies der Fall ist, öffnet der Dienstanbieter den seriellen Anschluss für das Modem und platziert den Ansichts Vorgang direkt in **linecallstate \_**. Die Anwendung kann dann die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion mit der Geräteklasse "comm/datamoder" verwenden, um ein geöffnetes Datei Handle zum Lesen aus dem und zum Schreiben in den Port "comm" zu erhalten.

Der Passthrough-Modus kann als Reaktion auf einen eingehenden Aufruf ebenfalls aufgerufen werden. Im allgemeinen rufen Anwendungen den Passthrough-Modus auf, während sich der Aufruf im **linecallstate- \_ Angebot** befindet, bevor der Aufruf beantwortet wurde. Anstatt [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)aufzurufen, ruft die Anwendung [**linesetcallparameterams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams)auf und übergibt " **linebearermode \_ Passthrough** " als *dwbearermode* -Parameter. Wenn dies der Fall ist, wie bei [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), wird der Anruf sofort in **linecallstate \_** eingefügt, der durch den Dienstanbieter verbunden ist, und die Anwendung kann mithilfe von [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)ein Handle für den geöffneten Port abrufen. Die **linesetcallparameams** -Funktion kann aufgerufen werden, wenn der Aufruf das **linecallstate- \_ Angebot**, **linecallstate \_ Accepted** oder **linecallstate \_ verbunden** ist.

Der Passthrough-Modus wird normalerweise durch Aufrufen von [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) für das von [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) abgerufenen Aufruf handle oder die erste [**Zeile \_ CallState**](line-callstate.md) -Nachricht beendet, wenn der Aufruf ein eingehender Aufruf war. Der Dienstanbieter schließt den Port und stellt das Modem in seinem Standardzustand wieder her. Die Anwendung muss [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) für das von [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)empfangene handle aufrufen.

Der Passthrough-Modus kann auch durch Aufrufen von " [**linesetcallparser**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) " beendet werden, wobei der Parameter " *dwbearermode* " auf " **linebearermode \_ Voice**" festgelegt ist Der Medientyp (-Modus), der von [**linesetmediamode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) festgelegt wird, wird als wirksam angenommen. Wenn **linemediamode \_ datamoder** aktiv ist, übernimmt der Dienstanbieter den Aufruf so, als ob es sich um einen bereits in Bearbeitung befindlichen Datenmodem Aufruf handelt. Wenn anschließend [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) aufgerufen wird, gibt der Dienstanbieter die entsprechenden Modem Befehle oder Schnittstellen Zustandsänderungen zum Löschen eines Daten Aufrufs aus.

> [!Note]  
> Wenn der Passthrough-Modus beendet wird, während der-Vorgang ausgeführt wird, kann der TAPI-Dienstanbieter (TSP) für die-Zeile die Modem Einstellungen in den Standardzustand zurückversetzen. Unimodem ist ein Beispiel für einen TSP, der die Modem Einstellungen beim Beenden des Passthrough-Modus immer wiederherstellt. Aus diesem Grund kann der Passthrough-Modus nicht als Methode zum Konfigurieren des Geräts verwendet werden. Der Passthrough-Modus sollte nur für unterschiedliche Aktivitäten verwendet werden, die als abgeschlossen angesehen werden können, wenn Passthrough beendet wird. Beispiele für Aktivitäten, die den Passthrough-Modus verwenden können, sind das Senden eines Fax oder das Abspielen von Wave/Audiodaten über ein proprietäres Modem Protokoll.

 

 

 
