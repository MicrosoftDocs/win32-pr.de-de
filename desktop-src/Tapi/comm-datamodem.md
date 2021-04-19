---
description: Die Geräteklasse "comm/datamoder" besteht aus DataModem-Geräten.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comm/datamoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343731"
---
# <a name="commdatamodem"></a>comm/datamoder

Die Geräteklasse "comm/datamoder" besteht aus DataModem-Geräten. Sie greifen auf diese Geräte mithilfe der [Datei](/windows/desktop/FileIO/file-management-functions) -und [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zu. Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ datamoder-Medientyp unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.

Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt **dwstringformat** auf den "StringFormat" \_ -Binärwert fest und fügt diese zusätzlichen Member an:

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

Der **hcomm** -Member ist das Handle des Open Communications-Ports. Dieser Member ist **null** , wenn der Anschluss noch nicht geöffnet ist, oder wenn der *dwselect* -Parameter von [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) nicht der linecallselect- \_ Aufrufwert ist. Wenn ein-Rückruf aktiv ist, öffnet der Dienstanbieter in der Regel den Port selbst, um die direkte Steuerung der Kommunikationshardware zu erhalten, ist jedoch nur erforderlich, um ein gültiges Handle zurückzugeben, wenn die Zeile verbunden ist. Der Dienstanbieter öffnet den Port mit dem überlappenden \_ Dateiflag \_ und konfiguriert dann den Port mit den Einstellungen, die von der [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) -Funktion angegeben werden. Sie können zusätzliche Konfigurationsoptionen für das Gerät festlegen, indem Sie Kommunikationsfunktionen mit dem zurückgegebenen Handle verwenden.

Der **szdevicename** -Member ist eine **null**-terminierte Zeichenfolge, die den Namen des Kommunikationsports angibt, der der Zeile, Adresse oder dem-Befehl zugeordnet ist.

Wenn **hcomm** ein gültiges Handle ist, können Sie es in nachfolgenden Aufrufen von Dateifunktionen wie "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" verwenden, um Daten für den Aufruf zu senden und zu empfangen. Wenn Sie den Kommunikationsport nicht mehr verwenden und vorzugsweise die [**linedeallo-eCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) -Funktion verwenden, um die Zuordnung des Aufrufes aufzurufen, müssen Sie den Port mit der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion schließen.

Bei Verwendung der Funktionen [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) und [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) ist es für einige Dienstanbieter erforderlich, dass die Konfigurationsdaten für diese Geräteklasse das folgende Format aufweisen:

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

Im folgenden finden Sie Informationen zur Gerätekonfiguration für die Verwendung mit den Funktionen [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) und [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Summe der Größe der **devcfghdr** -Struktur und der tatsächlichen Größe der [**CommConfig**](/windows/desktop/api/winbase/ns-winbase-commconfig) -Struktur.

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**
</dt> <dd>

Die Versionsnummer der Unimodem- **Devconfig** -Struktur. Dieser Member kann mdmcfg- \_ Version (0x00010003) sein.

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**"f"-Optionen**
</dt> <dd>

Optionsflags, die auf der Optionsseite Unimodem angezeigt werden. Dieser Member kann eine Kombination folgender Werte sein:

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>Terminal \_ vor (1)
</dt> <dd>

Zeigt den Bildschirm vor dem Terminal an.

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>Terminal \_ Post (2)
</dt> <dd>

Zeigt den Bildschirm nach dem Terminal an.

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>Manuelles \_ wählen (4)
</dt> <dd>

Gibt das Telefon manuell aus, wenn dies möglich ist.

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>Start \_ Beleuchtung (8)
</dt> <dd>

Zeigt das Modem Symbol im Statusbereich der Taskleiste an.

Nur der Wert für die Start \_ Beleuchtung ist standardmäßig festgelegt.

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wwaitbong**
</dt> <dd>

Anzahl von Sekunden (in zwei Sekunden, Granularität), um den warte Vorgang auf den Bonitäts Ton ($) zu ersetzen.

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**CommConfig**
</dt> <dd>

Die [**CommConfig**](/windows/desktop/api/winbase/ns-winbase-commconfig) -Struktur, die mit den Konfigurationsfunktionen für die Kommunikation und Modem verwendet werden kann.

</dd> </dl>

 

 
