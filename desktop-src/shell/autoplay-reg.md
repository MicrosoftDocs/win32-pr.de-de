---
description: Es gibt viele Situationen, in denen Autorun möglicherweise temporär oder dauerhaft deaktiviert werden muss.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Aktivieren und Deaktivieren von Autorun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393454"
---
# <a name="enabling-and-disabling-autorun"></a>Aktivieren und Deaktivieren von Autorun

Es gibt viele Situationen, in denen Autorun möglicherweise temporär oder dauerhaft deaktiviert werden muss. Autorun könnte z. b. den Betrieb einer laufenden Anwendung beeinträchtigen und muss für die Dauer deaktiviert werden. Das System bietet mehrere Möglichkeiten, Autorun zu deaktivieren.

-   [Programm gesteuertes unterdrücken von Autorun](#suppressing-autorun-programmatically)
-   [Verwenden der Registrierung zum Deaktivieren von Autorun](#using-the-registry-to-disable-autorun)
-   [Autorun für andere Typen von Speichermedien](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Programm gesteuertes unterdrücken von Autorun

Es gibt eine Vielzahl von Situationen, in denen Autorun möglicherweise Programm gesteuert unterdrückt werden muss. Zwei Beispiele:

-   Die Anwendung verfügt über ein Setup Programm, mit dem der Benutzer einen anderen Datenträger einfügen muss, der möglicherweise eine Autorun. inf-Datei enthält.
-   Während der Ausführung der Anwendung muss der Benutzer möglicherweise eine andere CD einfügen, die eine Autorun. inf-Datei enthalten kann.

In beiden Fällen möchten Sie normalerweise nicht eine andere Anwendung starten, während das Original ausgeführt wird.

Benutzer können Autorun manuell unterdrücken, indem Sie die UMSCHALTTASTE gedrückt halten, wenn Sie die CD-ROM einfügen. Es ist jedoch in der Regel besser, diesen Vorgang Programm gesteuert und nicht in Abhängigkeit vom Benutzer zu verarbeiten.

Bei Systemen mit der Shell- [Version 4,70](versions.md) und höher wird von Windows eine "querycancelautoplay"-Meldung an das Vordergrund Fenster gesendet. Die Anwendung kann auf diese Meldung reagieren, um Autorun zu unterdrücken. Diese Vorgehensweise wird von System Dienstprogrammen wie dem Dialogfeld zum [Öffnen](../dlgbox/open-and-save-as-dialog-boxes.md) von Common verwendet, um Autorun zu deaktivieren.

Die folgenden Code Fragmente veranschaulichen, wie Sie diese Nachricht einrichten und behandeln. Die Anwendung muss im Vordergrund Fenster ausgeführt werden. Registrieren Sie zuerst "querycancelautoplay" als Windows-Meldung:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



Das Fenster Ihrer Anwendung muss sich im Vordergrund befinden, um diese Meldung zu empfangen. Der Nachrichten Handler sollte **true** zurückgeben, um Autorun abzubrechen, und **false** , um ihn zu aktivieren. Im folgenden Code Fragment wird veranschaulicht, wie diese Meldung verwendet wird, um Autorun zu deaktivieren.


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



Wenn Ihre Anwendung ein Dialogfeld verwendet und auf eine "querycancelautoplay"-Meldung reagieren muss, kann Sie nicht einfach " **true** " oder " **false**" zurückgeben. Aufrufen Sie stattdessen [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , wobei *nIndex* auf **DWL \_ msgresult** festgelegt ist. Legen Sie für den Parameter " *dwnewlong* " den Wert " **true** " fest, um den **Vorgang zu beenden** . Beispielsweise wird beim Empfangen der Meldung "querycancelautoplay" die Autorun-Nachricht durch die folgende Beispiel Dialogfeld Prozedur abgebrochen.


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a>Verwenden der Registrierung zum Deaktivieren von Autorun

Es gibt zwei Registrierungs Werte, die verwendet werden können, um Autorun dauerhaft zu deaktivieren: NoDriveAutoRun und nodrivetypeer Autorun. Der erste Wert deaktiviert Autorun für angegebene Laufwerk Buchstaben, das zweite deaktiviert Autorun für eine Klasse von Laufwerken. Wenn einer dieser Werte so festgelegt ist, dass Autorun für ein bestimmtes Gerät deaktiviert wird, wird er deaktiviert. Weitere Informationen zum Deaktivieren der Autorun-Funktionalität finden Sie im Knowledge Base-Artikel [Deaktivieren der Autorun-Funktionalität in Windows](https://support.microsoft.com/kb/967715) . In diesem Artikel werden die verschiedenen Updates aufgelistet, die installiert sein müssen, um die Autorun-Funktionalität ordnungsgemäß zu deaktivieren.

> [!Note]  
> Die NoDriveAutoRun-und nodrivetypeer Autorun-Werte sollten nur von Systemadministratoren geändert werden, um den Wert für das gesamte System zu Test-oder Verwaltungszwecken zu ändern. Anwendungen sollten diese Werte nicht ändern, da es keine Möglichkeit gibt, Sie zuverlässig auf ihre ursprünglichen Werte wiederherzustellen.

 

Der NoDriveAutoRun-Wert deaktiviert Autorun für angegebene Laufwerk Buchstaben. Es handelt sich um einen reg \_ DWORD-Datenwert, der unter dem folgenden Schlüssel gefunden wird:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Das erste Bit des Werts entspricht Laufwerk A:, der zweiten zu B: usw. Um Autorun für einen oder mehrere Laufwerk Buchstaben zu deaktivieren, legen Sie die entsprechenden Bits fest. Wenn Sie z. b. die Laufwerke A: und C: deaktivieren möchten, legen Sie NoDriveAutoRun auf fest `0x00000005` .

Der nodrivetypeer Autorun-Wert deaktiviert Autorun für eine Klasse von Laufwerken. Dabei handelt es sich um einen reg \_ DWORD-oder 4-Byte-reg- \_ Binär Datenwert, der unter dem gleichen Schlüssel enthalten ist.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Durch Festlegen der Bits des ersten Byte dieses Werts können unterschiedliche Laufwerke von der Arbeit mit Autorun ausgeschlossen werden.

Die folgende Tabelle enthält die Bits-und Bitmasken Konstanten, die im ersten Byte von nodrivetypeer Autorun festgelegt werden können, um Autorun für einen bestimmten Laufwerkstyp zu deaktivieren. Sie müssen Windows-Explorer neu starten, damit die Änderungen wirksam werden.



| Bitzahl | Bitmasken Konstante      | BESCHREIBUNG                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **Laufwerks \_ Removeable** | Der Datenträger kann von einem Laufwerk (z. b. einem Diskettenlaufwerk) entfernt werden. |
| 0x08       | **Laufwerk \_ korrigiert**      | Der Datenträger kann nicht vom Laufwerk (einer Festplatte) entfernt werden.        |
| 0x10       | **Laufwerk \_ Remote**     | Netzwerklaufwerk.                                          |
| 0x20       | **Laufwerk- \_ CDROM**      | CD-ROM-Laufwerk                                           |
| 0x40       | **Laufwerk \_ Ramdisk**    | RAM-Datenträger.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>Autorun für andere Typen von Speichermedien

Autorun ist hauptsächlich für die öffentliche Verteilung von Anwendungen auf CD-ROM und DVD-ROM gedacht, und die Verwendung wird von anderen Speichermedien abgeraten. Es ist jedoch oft hilfreich, Autorun auf anderen Typen von Wechselmedien zu aktivieren. Diese Funktion wird normalerweise verwendet, um das Debuggen von Autorun-INF-Dateien zu vereinfachen. Autorun funktioniert nur auf Wechsel Datenträgern, wenn die folgenden Kriterien erfüllt sind:

-   Das Gerät muss über Auto-kompatible Treiber verfügen. Damit ein Treiber nicht kompatibel ist, muss er vom System benachrichtigt werden, dass ein Datenträger eingefügt wurde, indem eine [**WM \_ devicechange**](../devio/wm-devicechange.md) -Nachricht gesendet wird.
-   Das Stammverzeichnis des eingefügten Mediums muss eine Autorun. inf-Datei enthalten.
-   Das Gerät darf nicht durch die [Registrierung](#using-the-registry-to-disable-autorun)deaktiviert werden.
-   Die Vordergrund Anwendung hat Autorun nicht unter [drückt](#suppressing-autorun-programmatically) .

> [!Note]  
> Diese Funktion sollte nicht zum Verteilen von Anwendungen auf Wechselmedien verwendet werden. Da das Implementieren von Autorun auf Wechsel Datenträgern eine einfache Möglichkeit zum Verteilen von Computerviren darstellt, sollten die Benutzer für jede öffentlich verteilte Diskette, die eine Autorun. inf-Datei enthält, verdächtig sein.

 

Normalerweise startet Autorun automatisch, kann aber auch manuell gestartet werden. Wenn das Gerät die oben aufgeführten Kriterien erfüllt, enthält das Kontextmenü des Laufwerk Buchstabens einen **AutoPlay** -Befehl. Um Autorun manuell auszuführen, klicken Sie entweder mit der rechten Maustaste auf das Laufwerk Symbol, und wählen Sie im Kontextmenü die Option **AutoPlay** aus, oder Doppelklicken Sie auf das Laufwerk Symbol. Wenn die Treiber nicht automatisch kompatibel sind, enthält das Kontextmenü kein **AutoPlay** -Element, und Autorun kann nicht gestartet werden.

Auto-kompatible Treiber werden mit einigen Wechsel Datenträgern bereitgestellt, sowie einigen anderen Typen von Wechselmedien wie z. b. "CompactFlash Cards". Autorun funktioniert auch mit Netzwerklaufwerken, die einem Laufwerk Buchstaben mit Windows-Explorer zugeordnet sind oder mit der [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)eingebunden sind. Wie bei der bereitgestellten Hardware muss ein bereitgestelltes Netzwerklaufwerk über eine Autorun. inf-Datei im Stammverzeichnis verfügen, und es darf nicht über die [Registrierung](#using-the-registry-to-disable-autorun)deaktiviert werden.

 

 
