---
description: Es gibt viele Situationen, in denen autoRun vorübergehend oder dauerhaft deaktiviert werden muss.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Aktivieren und Deaktivieren von AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd14a1dfd3aadb94f3586dec783ea6d394f717f500b5ac103c65fcb813baf14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090780"
---
# <a name="enabling-and-disabling-autorun"></a>Aktivieren und Deaktivieren von AutoRun

Es gibt viele Situationen, in denen autoRun vorübergehend oder dauerhaft deaktiviert werden muss. AutoRun kann z. B. den Betrieb einer ausgeführten Anwendung beeinträchtigen und muss für die Dauer deaktiviert werden. Das System bietet mehrere Möglichkeiten, autoRun zu deaktivieren.

-   [Programmgesteuertes Unterdrücken der automatischen Ausführen](#suppressing-autorun-programmatically)
-   [Verwenden der Registrierung zum Deaktivieren der automatischen Verwendung](#using-the-registry-to-disable-autorun)
-   [Automatisches Ausführen für andere Arten Storage Medien](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Programmgesteuertes Unterdrücken der automatischen Ausführen

Es gibt eine Vielzahl von Situationen, in denen AutoRun programmgesteuert unterdrückt werden muss. Zwei Beispiele:

-   Ihre Anwendung verfügt über ein Setupprogramm, bei dem der Benutzer einen anderen Datenträger einfügen muss, der eine Autorun.inf-Datei enthalten kann.
-   Während des Anwendungsbetriebs muss der Benutzer möglicherweise einen weiteren Datenträger einfügen, der eine Autorun.inf-Datei enthalten kann.

In beiden Fällen möchten Sie normalerweise keine andere Anwendung starten, während die ursprüngliche Anwendung in Bearbeitung ist.

Benutzer können AutoRun manuell unterdrücken, indem sie beim Einfügen der CD-ROM die UMSCHALTTASTE halten. Es ist jedoch in der Regel vorzuziehen, diesen Vorgang programmgesteuert und nicht abhängig vom Benutzer zu behandeln.

Bei Systemen mit [Shell-Version 4.70](versions.md) und höher sendet Windows eine "QueryCancelAutoPlay"-Nachricht an das Vordergrundfenster. Ihre Anwendung kann auf diese Meldung reagieren, um autoRun zu unterdrücken. Dieser Ansatz wird von Systemprogrammen wie dem Dialogfeld Allgemein [öffnen](../dlgbox/open-and-save-as-dialog-boxes.md) verwendet, um autoRun zu deaktivieren.

Die folgenden Codefragmente veranschaulichen, wie diese Meldung eingerichtet und behandelt wird. Ihre Anwendung muss im Vordergrundfenster ausgeführt werden. Registrieren Sie zuerst "QueryCancelAutoPlay" als Windows Nachricht:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



Das Fenster Ihrer Anwendung muss sich im Vordergrund befindet, um diese Nachricht zu empfangen. Der Meldungshandler sollte **TRUE zurückgeben,** um autoRun abzubricht, **und FALSE,** um es zu aktivieren. Das folgende Codefragment veranschaulicht, wie Diese Meldung verwendet wird, um autoRun zu deaktivieren.


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



Wenn Ihre Anwendung ein Dialogfeld verwendet und auf eine "QueryCancelAutoPlay"-Meldung antworten muss, kann sie nicht einfach **TRUE** oder **FALSE zurückgeben.** Rufen Sie stattdessen [**SetWindowLong auf,**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) bei *dem nIndex* auf **DWL \_ MSGRESULT festgelegt ist.** Legen Sie *den dwNewLong-Parameter* auf **TRUE fest,** um autoRun abzubruchen, und **FALSE,** um ihn zu aktivieren. Die folgende Beispieldialogfeldprozedur bricht beispielsweise autoRun ab, wenn die Meldung "QueryCancelAutoPlay" empfangen wird.


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



## <a name="using-the-registry-to-disable-autorun"></a>Verwenden der Registrierung zum Deaktivieren der automatischen Verwendung

Es gibt zwei Registrierungswerte, mit denen AutoRun dauerhaft deaktiviert werden kann: NoDriveAutoRun und NoDriveTypeAutoRun. Der erste Wert deaktiviert AutoRun für angegebene Laufwerkbuchstaben, und der zweite Wert deaktiviert AutoRun für eine Klasse von Laufwerken. Wenn einer dieser Werte so festgelegt ist, dass autoRun für ein bestimmtes Gerät deaktiviert wird, wird er deaktiviert. Weitere Informationen zum Deaktivieren Windows AutoRun-Funktionalität finden Sie im Knowledge Base Deaktivieren der AutoRun-Funktion [in](https://support.microsoft.com/kb/967715) Windows In diesem Artikel. In diesem Artikel werden die verschiedenen Updates aufgeführt, die Sie installiert haben müssen, um die Funktion Autorun ordnungsgemäß zu deaktivieren.

> [!Note]  
> Die Werte NoDriveAutoRun und NoDriveTypeAutoRun sollten nur von Systemadministratoren geändert werden, um den Wert für das gesamte System zu Test- oder Verwaltungszwecken zu ändern. Anwendungen sollten diese Werte nicht ändern, da es keine Möglichkeit gibt, sie zuverlässig auf ihre ursprünglichen Werte wiederherzustellen.

 

Der Wert NoDriveAutoRun deaktiviert AutoRun für angegebene Laufwerkbuchstaben. Dabei handelt es sich um \_ einen REG DWORD-Datenwert, der sich unter dem folgenden Schlüssel befindet:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Das erste Bit des Werts entspricht Laufwerk A:, das zweite B:, und so weiter. Legen Sie die entsprechenden Bits fest, um AutoRun für einen oder mehrere Laufwerkbuchstaben zu deaktivieren. Um beispielsweise die Laufwerke A: und C: zu deaktivieren, legen Sie NoDriveAutoRun auf `0x00000005` fest.

Der Wert NoDriveTypeAutoRun deaktiviert AutoRun für eine Klasse von Laufwerken. Es handelt sich um einen REG \_ DWORD- oder 4-Byte-REG \_ BINARY-Datenwert, der unter demselben Schlüssel gefunden wird.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Durch Festlegen der Bits des ersten Byte dieses Werts können verschiedene Laufwerke von der Arbeit mit AutoRun ausgeschlossen werden.

Die folgende Tabelle enthält die Bits- und Bitmaskenkonstituen, die im ersten Byte von NoDriveTypeAutoRun festgelegt werden können, um AutoRun für einen bestimmten Laufwerktyp zu deaktivieren. Sie müssen den Windows-Explorer neu starten, bevor die Änderungen wirksam werden.



| Bitnummer | Bitmaskenkonst constant      | BESCHREIBUNG                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **LAUFWERK \_ ENTFERNBAR** | Der Datenträger kann vom Laufwerk entfernt werden (z. B. ein Diskettenlaufwerk). |
| 0x08       | **LAUFWERK \_ FEST**      | Der Datenträger kann nicht vom Laufwerk (einer Festplatte) entfernt werden.        |
| 0x10       | **LAUFWERK \_ REMOTE**     | Netzwerklaufwerk.                                          |
| 0x20       | **\_LAUFWERKS-C LAUFWERK**      | CD-ROM-Laufwerk                                           |
| 0x40       | **LAUFWERK \_ RAMDISK**    | RAM-Datenträger.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>Automatisches Ausführen für andere Arten Storage Medien

AutoRun ist hauptsächlich für die öffentliche Verteilung von Anwendungen auf CD-ROM und DVD-ROM vorgesehen, und von der Verwendung für andere Speichermedien wird abgeraten. Es ist jedoch häufig hilfreich, AutoRun auf anderen Wechselmedien zu aktivieren. Dieses Feature wird in der Regel verwendet, um das Debuggen von AutoRun.inf-Dateien zu vereinfachen. AutoRun funktioniert nur auf Wechselmedien, wenn die folgenden Kriterien erfüllt sind:

-   Das Gerät muss über AutoRun-kompatible Treiber verfügen. Um autoRun-kompatibel zu sein, muss ein Treiber das System benachrichtigen, dass ein Datenträger eingefügt wurde, indem er eine [**WM \_ DEVICECHANGE-Nachricht**](../devio/wm-devicechange.md) sendet.
-   Das Stammverzeichnis des eingefügten Mediums muss eine Autorun.inf-Datei enthalten.
-   Auf dem Gerät darf autoRun nicht über die Registrierung [deaktiviert sein.](#using-the-registry-to-disable-autorun)
-   Die Vordergrundanwendung hat autoRun [nicht](#suppressing-autorun-programmatically) unterdrückt.

> [!Note]  
> Dieses Feature sollte nicht zum Verteilen von Anwendungen auf Wechselmedien verwendet werden. Da die Implementierung von AutoRun auf Wechselmedien eine einfache Möglichkeit zum Verteilen von Computerviren bietet, sollten Benutzer verdächtig gegenüber öffentlich verteilten Disketten sein, die eine Autorun.inf-Datei enthalten.

 

Normalerweise wird AutoRun automatisch gestartet, kann aber auch manuell gestartet werden. Wenn das Gerät die oben aufgeführten Kriterien erfüllt, enthält das Kontextmenü des Laufwerkbuchstabens einen **AutoPlay-Befehl.** Klicken Sie zum manuellen Ausführen von AutoRun entweder mit der rechten Maustaste auf das Laufwerksymbol, und wählen Sie im Kontextmenü **AutoPlay** aus, oder doppelklicken Sie auf das Laufwerksymbol. Wenn die Treiber nicht autoRun-kompatibel sind, hat das Kontextmenü kein **AutoPlay-Element,** und AutoRun kann nicht gestartet werden.

AutoRun-kompatible Treiber werden mit einigen Wechseldatenträgern sowie einigen anderen Wechselmedien wie CompactFlash-Karten bereitgestellt. AutoRun funktioniert auch mit Netzwerklaufwerken, die einem Laufwerkbuchstaben mit Windows Explorer zugeordnet oder mit dem Microsoft Management Console [(MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)bereitgestellt werden. Wie bei der bereitgestellten Hardware muss ein bereitgestelltes Netzwerklaufwerk über die Datei Autorun.inf im Stammverzeichnis verfügen und darf nicht über die Registrierung deaktiviert [werden.](#using-the-registry-to-disable-autorun)

 

 
