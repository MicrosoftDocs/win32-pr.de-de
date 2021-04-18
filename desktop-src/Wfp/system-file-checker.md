---
description: Mit dem System File Checker-Hilfsprogramm (Sfc.exe) können Administratoren alle geschützten Ressourcen überprüfen, um Ihre Versionen zu überprüfen.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: System File Checker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351120"
---
# <a name="system-file-checker"></a>System File Checker

Mit dem System File Checker-Hilfsprogramm (Sfc.exe) können Administratoren alle geschützten Ressourcen überprüfen, um Ihre Versionen zu überprüfen.

Dateien, die für den Neustart von Fenstern wichtig sind und nicht mit der erwarteten Windows-Version identisch sind, können durch die richtigen Versionen ersetzt werden. Wenn eine Datei repariert wird, werden auch die entsprechenden Registrierungsdaten repariert. Geschützte Dateien, die für den Neustart von Windows nicht wichtig sind, werden nicht repariert

## <a name="syntax"></a>Syntax

Im folgenden finden Sie die Befehlszeilen Syntax für SFC.

**SFC-Optionen \[ = Vollständiger Dateipfad\]**

## <a name="options"></a>Optionen

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CacheSize =*x*
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Legt die Dateicache Größe fest. Die Standardgröße des Caches beträgt 0x32 (50 MB).

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

Dieser Wert wird nicht unterstützt.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/ENABLE
</dt> <dd>

Dieser Wert wird nicht unterstützt.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

Nur Dateien überprüfen oder reparieren. Überprüfen oder reparieren Sie keine Registrierungsschlüssel.

**Windows XP:** Nicht unterstützt.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Verwenden Sie diese Option für Offline Reparaturen. Geben Sie den Speicherort des Offline-Start Verzeichnisses an.

**Windows XP:** Nicht unterstützt.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Verwenden Sie diese Option für Offline Reparaturen. Geben Sie den Speicherort des Windows-offline Verzeichnisses an.

**Windows XP:** Nicht unterstützt.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Leert den Dateicache und scannt alle geschützten Systemdateien.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/Quiet
</dt> <dd>

Dieser Wert wird nicht unterstützt.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Kehren Sie zu den Standardeinstellungen zurück.

**Windows Server 2008 und Windows Vista:** Nicht unterstützt.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Scannt alle geschützten Systemdateien bei jedem Start.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Scannt und repariert die Datei, die sich unter dem angegebenen vollständigen Pfad befindet.

**Windows XP:** Nicht unterstützt.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Scannt alle geschützten Systemdateien sofort.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Scannt beim nächsten Start alle geschützten Systemdateien.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Überprüft die Datei am angegebenen vollständigen Pfad. Mit dieser Option wird die Datei nicht repariert.

**Windows XP:** Nicht unterstützt.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Scannt alle geschützten Systemdateien, repariert jedoch keine Dateien.

**Windows XP:** Nicht unterstützt.

</dd> </dl>

SFC legt den folgenden Registrierungs Wert fest:

 = HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SfcScan

Weitere Informationen finden Sie unter [WFP-Registrierungs Werte](wfp-registry-values.md).

## <a name="remarks"></a>Bemerkungen

Nur unter Windows Vista können Sie die Umgebungsvariable **Windows \_ Tracing \_ logfile** auf den Speicherort eines gültigen Verzeichnisses festlegen, um eine Protokolldatei zu erhalten.

## <a name="examples"></a>Beispiele

Die folgenden Beispiel Befehlszeilen sind Beispiele für sfc.exe-Syntax.

**sfc-/scannow**

**SFC/VERIFYFILE = c: \\ Windows \\ system32 \\kernel32.dll**

**SFC/SCANFILE = d: \\ Windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**

**SFC/VERIFYONLY/FILESONLY**

 

 



