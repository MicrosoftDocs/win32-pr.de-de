---
description: Mit dem Hilfsprogramm für die Systemdateiüberprüfung Sfc.exe können Administratoren alle geschützten Ressourcen überprüfen, um ihre Versionen zu überprüfen.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: System File Checker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f751aa30c06dbff90b8d5221974236b45edf9f0f278c144f755568a0040f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330282"
---
# <a name="system-file-checker"></a>System File Checker

Mit dem Hilfsprogramm für die Systemdateiüberprüfung Sfc.exe können Administratoren alle geschützten Ressourcen überprüfen, um ihre Versionen zu überprüfen.

Dateien, die für einen Neustart Windows wichtig sind, die nicht mit der erwarteten Windows Version übereinstimmen, werden möglicherweise durch die richtigen Versionen ersetzt. Wenn eine Datei repariert wird, werden auch die entsprechenden Registrierungsdaten repariert. Geschützte Dateien, die für einen Neustart nicht wichtig sind, Windows nicht repariert werden.

## <a name="syntax"></a>Syntax

Im Folgenden ist die Befehlszeilensyntax für Sfc angegeben.

**SFC options \[ =full file path\]**

## <a name="options"></a>Optionen

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Legt die Größe des Dateicaches fest. Die Standardgröße des Caches ist 0x32 (50 MB).

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

Überprüfen oder reparieren Sie nur Dateien. Überprüfen oder reparieren Sie Registrierungsschlüssel nicht.

**Windows XP:** Wird nicht unterstützt.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Verwenden Sie diese Option für Offlinereparaturen. Geben Sie den Speicherort des Offlinestartverzeichnisses an.

**Windows XP:** Wird nicht unterstützt.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Verwenden Sie diese Option für Offlinereparaturen. Geben Sie den Speicherort des Offlineverzeichnisses Windows an.

**Windows XP:** Wird nicht unterstützt.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Leert den Dateicache und scannt alle geschützten Systemdateien.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Dieser Wert wird nicht unterstützt.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Kehren Sie zu den Standardeinstellungen zurück.

**Windows Server 2008 und Windows Vista:** Wird nicht unterstützt.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Dieser Wert wird nicht unterstützt.

**Windows Server 2003 und Windows XP:** Scannt bei jedem Start alle geschützten Systemdateien.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Überprüft und repariert die Datei unter dem angegebenen vollständigen Pfad.

**Windows XP:** Wird nicht unterstützt.

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

Überprüft die Datei unter dem angegebenen vollständigen Pfad. Mit dieser Option wird die Datei nicht repariert.

**Windows XP:** Wird nicht unterstützt.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Scannt alle geschützten Systemdateien, repariert aber keine Dateien.

**Windows XP:** Wird nicht unterstützt.

</dd> </dl>

Sfc legt den folgenden Registrierungswert fest:

 = HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCScan

Weitere Informationen finden Sie unter [WFP-Registrierungswerte.](wfp-registry-values.md)

## <a name="remarks"></a>Hinweise

Nur auf Windows Vista können Sie die Umgebungsvariable **WINDOWS \_ TRACING \_ LOGFILE** auf den Speicherort eines gültigen Verzeichnisses festlegen, um eine Protokolldatei zu empfangen.

## <a name="examples"></a>Beispiele

Die folgenden Beispielbefehlszeilen sind Beispiele für sfc.exe Syntax.

**sfc /SCANNOW**

**sfc /VERIFYFILE=c: \\ windows \\ system32 \\kernel32.dll**

**sfc /SCANFILE=d: \\ windows \\ system32 \\kernel32.dll /OFFBOOTDIR=d: \\ /OFFWINDIR=d: \\ windows**

**sfc /VERIFYONLY /FILESONLY**

 

 



