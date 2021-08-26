---
title: Syntax
description: Hier ist die Syntax zum Aufrufen von FXC.exe, dem Effektcompilertool. Ein Beispiel finden Sie unter Offline-Kompilierung.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9cae0305a8fdca5c9fd419cf610b0ebbb547331
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880771"
---
# <a name="syntax"></a>Syntax

Hier ist die Syntax zum Aufrufen von FXC.exe, dem Effektcompilertool. Ein Beispiel finden Sie unter [Offline-Kompilieren von](dx-graphics-tools-fxc-using.md).

-   [Verwendung](#usage)
-   [Argumente](#arguments)
-   [Anmerkungen](#remarks)
-   [Profiles](#profiles)
-   [Versionshinweise](#version-notes)
-   [Zugehörige Themen](#related-topics)

## <a name="usage"></a>Verwendung

**fxc** *SwitchOptions* *Filenames*

## <a name="arguments"></a>Argumente
Trennen Sie jede Switchoption durch ein Leerzeichen oder einen Doppelpunkt.

### <a name="switchoptions"></a>*SwitchOptions*
\[in \] Kompilierungsoptionen. Es gibt nur eine erforderliche Option, und viele weitere sind optional. Trennen Sie jedes durch ein Leerzeichen oder einen Doppelpunkt.

#### <a name="required-option"></a>Erforderliche Option
##### <a name="t-profile"></a>/T <*Profil*>
Shadermodell (siehe [Profile).](#profiles)

#### <a name="optional-options"></a>Optionale Optionen
##### <a name="-help"></a>/?, /help
Drucken Sie die Hilfe für `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*command.option.file*>
Datei, die zusätzliche Kompilierungsoptionen enthält. Diese Option kann mit anderen Befehlszeilenkompilierungsoptionen kombiniert werden. *"command.option.file"* darf nur eine Option pro Zeile enthalten. *"command.option.file"* darf keine leeren Zeilen enthalten. In der Datei angegebene Optionen dürfen keine führenden oder nachgestellten Leerzeichen enthalten.

##### <a name="all_resources_bound"></a>/all_resources_bound
Aktivieren Sie aggressives Abflachen in SM5.1+. Neu für Direct3D 12.

##### <a name="cc"></a>/Cc
Ausgabe der farbcodierten Assembly.

##### <a name="compress"></a>/compress
Dx10-Shader-Bytecode aus Dateien komprimieren.

##### <a name="d-idtext"></a>/D <*ID-Text* >=< >
Definieren Sie das Makro.

##### <a name="decompress"></a>/decompress
Dekomprimieren Sie dx10 shader bytecode aus der ersten Datei. Ausgabedateien sollten in der Reihenfolge aufgeführt werden, in der sie sich während der Komprimierung befanden.

##### <a name="dumpbin"></a>/dumpbin
Lädt eine Binärdatei, anstatt einen Shader zu kompilieren.

##### <a name="e-ltnamegt"></a>&lt;/E-Name&gt;
Shadereinstiegspunkt. Wenn kein Einstiegspunkt angegeben wird, wird **main** als Shadereintragsname betrachtet.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Aktiviert ungebundene Deskriptortabellen. Neu für Direct3D 12.

##### <a name="extractrootsignature-file"></a>/extractrootsignature *<-Datei*>
Extrahieren Sie die Stammsignatur aus dem Shader-Bytecode. Neu für Direct3D 12.

##### <a name="fc-file"></a>/Fc *<-Datei*>
Ausgabeassemblycodeauflistungsdatei.

##### <a name="fd-file"></a>/Fd *<-Datei*>
Extrahieren Sie Die Informationen zur Shader-Programmdatenbank (PDB), und schreiben Sie in die angegebene Datei. Wenn Sie den Shader kompilieren, verwenden Sie /Fd, um eine PDB-Datei mit Shaderdebuginformationen zu generieren.

##### <a name="fe-file"></a>/Fe *<-Datei*>
Ausgeben von Warnungen und Fehlern an die angegebene Datei.

##### <a name="fh-file"></a>Datei "/Fh  <">
Ausgabeheaderdatei mit Objektcode.

##### <a name="fl-file"></a>/Fl *<-Datei*
Ausgabe einer Bibliothek. Erfordert den D3dcompiler \_47.dll oder eine höhere Version der DLL.

##### <a name="fo-file"></a>/Fo *<-Datei*>
Ausgabeobjektdatei. Häufig mit der Erweiterung &quot; .fxc, &quot; obwohl andere Erweiterungen verwendet werden, &quot; z. B. &quot; O, &quot; OBJ oder &quot; &quot; &quot; DXBC.

##### <a name="fx-file"></a>/Fx *<-Datei*>
Ausgabeassemblycode und hexadezimale Auflistungsdatei.

##### <a name="gch"></a>/Gch
Kompilieren Sie als untergeordneten Effekt für fx_4_x Profile.

> [!NOTE]
> Die Unterstützung von Legacyeffektprofilen ist veraltet.

##### <a name="gdp"></a>/Bip
Deaktivieren Sie den Effektleistungsmodus.

##### <a name="gec"></a>/Gec
Aktivieren Sie den Abwärtskompatibilitätsmodus.

##### <a name="ges"></a>/Ges
Aktivieren Sie den Strict-Modus.

##### <a name="getprivate-file"></a>/getprivate *<-Datei*>
Speichern Sie private Daten aus dem Shaderblob (kompilierte Shaderbinärdatei) in der angegebenen Datei. Extrahiert private Daten, die zuvor durch /setprivate eingebettet wurden, aus dem Shaderblob.

Sie müssen die Option /dumpbin mit /getprivate angeben. Beispiel:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Vermeiden Sie Flusssteuerungskonstrukte.

##### <a name="gfp"></a>/Soll
Flusssteuerungskonstrukte bevorzugen.

##### <a name="gis"></a>/Js
Erzwingen Sie IEEE-Strenge.

##### <a name="gpp"></a>/Gpp
Erzwingen Sie partielle Genauigkeit.
    
##### <a name="i-include"></a>/I <*include*>
Zusätzlicher Includepfad.

##### <a name="lx"></a>/Lx
Gibt Hexadezimalliterale aus. Erfordert den D3dcompiler \_47.dll oder eine höhere Version der DLL.

##### <a name="matchuavs"></a>/matchUAVs
Übereinstimmung mit UAV-Slotzuordnungen des Vorlagen-Shaders im aktuellen Shader. Weitere Informationen finden Sie unter <a href="#remarks">Hinweise.</a>

##### <a name="mergeuavs"></a>/mergeUAVs
Zusammenführen von UAV-Slotzuordnungen des Vorlagen-Shaders und des aktuellen Shaders. Weitere Informationen finden Sie unter <a href=""></a> <a href="#remarks">Hinweise.</a>

##### <a name="ni"></a>/Ni
Ausgabeanweisungsnummern in Assemblyauflistungen.

##### <a name="no"></a>/No
Ausgabeanweisungs-Byteoffset in Assemblyauflistungen. Wenn Sie eine Assembly erstellen, verwenden Sie /No, um sie mit dem Byteoffset für jede Anweisung zu versehen.

##### <a name="nologo"></a>/nologo
Copyrightmeldung unterdrücken

##### <a name="od"></a>/Od
Deaktiviert Optimierungen. /Od impliziert /Stufen, obwohl die Ausgabe möglicherweise nicht identisch mit /Od /Soll ist.

##### <a name="op"></a>/Op
Deaktivieren Von Preshadern (veraltet)

##### <a name="o0-o1-o2-o3"></a>/O0 /O1, /O2, /O3
Optimierungsebenen. O1 ist die Standardeinstellung.
- O0: Deaktiviert die Neuanordnung von Anweisungen. Dies trägt dazu bei, die Registerlast zu reduzieren und eine schnellere Schleifensimulation zu ermöglichen.
- O1: Deaktiviert die Neuanordnung von Anweisungen für ps_3_0 und nach oben.
- O2 : Identisch mit O1. Für die zukünftige Verwendung reserviert.
- O3 – identisch mit O1. Für die zukünftige Verwendung reserviert.

##### <a name="p-file"></a>/P *<-Datei*>
Vorverarbeiten in eine Datei (muss allein verwendet werden).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Entfernt Debugdaten aus shader-Bytecode für Profile mit mehr als 4_0.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Entfernt die privaten Daten aus dem 4_0+-Shader-Bytecode. Entfernt private Daten (beliebige Bytesequenz) aus dem Shaderblob (kompilierte Shaderbinärdatei), die Sie zuvor mit der -Option eingebettet `/setprivate <file>` haben.

Sie müssen die Option /dumpbin mit /Qstrip_priv angeben. Beispiel:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Strip reflection data from shader bytecode for 4_0+ profiles(Abblenden von Reflektionsdaten aus shader bytecode für Profile mit mehr als 4_0).

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Entfernt die Stammsignatur aus dem Shader-Bytecode. Neu für Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Angenommen, UAVs/SRVs können alias für cs_5_0+ sein. Erfordert die D3dcompiler-47.dll \_ oder eine höhere Version der DLL.

##### <a name="setprivate-file"></a>/setprivate *<-Datei*>
Fügen Sie dem kompilierten Shaderblob private Daten in der angegebenen Datei hinzu. Bettet die angegebene Datei, die als roher Puffer behandelt wird, in das Shaderblob ein. Verwenden Sie /setprivate, um private Daten hinzuzufügen, wenn Sie einen Shader kompilieren. Verwenden Sie alternativ die Option /dumpbin mit /setprivate, um ein vorhandenes Shaderobjekt zu laden, und fügen Sie dann das private Datenblob hinzu, nachdem sich das Objekt im Arbeitsspeicher befindet. Verwenden Sie beispielsweise einen einzelnen Befehl mit /setprivate, um einem kompilierten Shaderblob private Daten hinzuzufügen:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
Oder verwenden Sie zwei Befehle, bei denen der zweite Befehl ein Shaderobjekt lädt und dann private Daten hinzufügt:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>/setrootsignature *<-Datei*>
Fügt die Stammsignatur an Shader-Bytecode an. Neu für Direct3D 12.

##### <a name="shtemplate-file"></a>/shtemplate *<-Datei*>
Verwenden Sie eine angegebene Vorlagen-Shaderdatei zum Zusammenführen (/mergeUAVs) und zum Abgleichen (/matchUAVs) von Ressourcen. Weitere Informationen finden Sie unter <a href="#remarks">Hinweise.</a>

##### <a name="vd"></a>/Vd
Deaktivieren Sie die Überprüfung.

##### <a name="verifyrootsignature-file"></a>/verifyrootsignature *<-Datei*>
Überprüfen Sie den Shader-Bytecode anhand der Stammsignatur. Neu für Direct3D 12.

##### <a name="vi"></a>/Vi
Zeigt Details zum Includeprozess an.

##### <a name="vn-name"></a>/Vn <*Name*>
Verwenden Sie name als Variablennamen in der Headerdatei.

##### <a name="wx"></a>/WX
Warnungen werden als Fehler behandelt.

##### <a name="zi"></a>/ZI
Aktiviert Debuginformationen.

##### <a name="zpc"></a>/Zpc
Packen Sie Matrizen in Spaltenhauptreihenfolge.

##### <a name="zpr"></a>/Zpr
Packen Sie Matrizen in Zeilenreihenfolge.

### <a name="filenames"></a>*Dateinamen*

\[in \] Die Dateien, die die Shader und/oder die Auswirkungen enthalten.

## <a name="remarks"></a>Hinweise

Verwenden Sie die `/mergeUAVs` Optionen , und , um die `/matchUAVs` `/shtemplate` UAV-Bindungsslots für eine Kette von Shadern auszurichten.

Angenommen, Sie verfügen über die Shader A.fx, B.fx und C.fx. Um die UAV-Bindungsslots für diese Shaderkette auszurichten, benötigen Sie zwei Kompilierungsdurchläufe:

**So richten Sie die UAV-Bindungsslots für eine Kette von Shadern aus**

1.  Verwenden Sie /mergeUAVs, um Shader zu kompilieren, und geben Sie ein zuvor kompiliertes Shaderblob mit /shtemplate an. Beispiel:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Verwenden Sie /matchUAVs, um Shader zu kompilieren, und geben Sie das letzte Shaderblob aus dem ersten Durchlauf mit /shtemplate an. Sie können in beliebiger Reihenfolge kompilieren. Beispiel:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
Sie müssen C.fx im zweiten Durchlauf nicht erneut kompilieren.

Nachdem Sie die beiden vorherigen Kompilierungsdurchläufe ausgeführt haben, können Sie A.o, B.o und C.o als endgültige Shaderblobs mit ausgerichteten UAV-Slots verwenden.

## <a name="profiles"></a>Profiles

Jedes Shadermodell wird mit einem HLSL-Profil bezeichnet. Um einen Shader für ein bestimmtes Shadermodell zu kompilieren, wählen Sie das entsprechende Shaderprofil aus der folgenden Tabelle aus.

<table><thead><tr class="header"><th>Shadertyp</th><th>Profiles</th></tr></thead><tbody><tr class="odd"><td>Compute-Shader</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>Domain-Shader</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>Geometrie-Shader</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>HLSL-Shaderverknüpfung </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Weitere Informationen zur Shaderverknüpfung finden Sie unter <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> und <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph.</strong></a> <br/></td></tr><tr class="odd"><td>Rumpf-Shader</td><td><dl> hs_5_0<br />
hs_5_1<br />
</dl></td></tr><tr class="even"><td>Pixelshader</td><td><dl> ps_2_0<br />
ps_2_a<br />
ps_2_b<br />
ps_2_sw<br />
ps_3_0<br />
ps_3_sw<br />
ps_4_0<br />
ps_4_0_level_9_0<br />
ps_4_0_level_9_1<br />
ps_4_0_level_9_3<br />
ps_4_1<br />
ps_5_0<br />
ps_5_1<br />
</dl></td></tr><tr class="odd"><td>Stammsignatur</td><td><dl> rootsig_1_0<br />
</dl></td></tr><tr class="even"><td>Textur-Shader</td><td><dl> tx_1_0<br />
</dl></td></tr><tr class="odd"><td>Vertexshader</td><td><dl> vs_1_1<br />
vs_2_0<br />
vs_2_a<br />
vs_2_sw<br />
vs_3_0<br />
vs_3_sw<br />
vs_4_0<br />
vs_4_0_level_9_0<br />
vs_4_0_level_9_1<br />
vs_4_0_level_9_3<br />
vs_4_1<br />
vs_5_0<br />
vs_5_1<br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a>Versionshinweise

Informationen zu Direct3D 12 finden Sie unter [Angeben von Stammsignaturen in HLSL,](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl) [Ressourcenbindung in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) und [dynamische Indizierung mit HLSL 5.1.](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1)

Verwenden Sie in Direct3D 10 die API, um das Scheitelpunkt-, Geometrie- und Pixelshaderprofil abzurufen, das für ein bestimmtes Gerät am besten geeignet ist, indem Sie diese Funktionen aufrufen: [**D3D10GetVertexShaderProfile,**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile) [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)und [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

Verwenden Sie in Direct3D 9 die [**Methoden GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) oder [**GetDeviceCaps,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) um die von einem Gerät unterstützten Scheitelpunkt- und Pixel-Shaderprofile abzurufen. Die von diesen Methoden [**zurückgegebene D3DCAPS9-Struktur**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) gibt die Scheitelpunkt- und Pixelshaderprofile an, die von einem Gerät in den **Membern VertexShaderVersion** und **PixelShaderVersion** unterstützt werden.

Beispiele finden Sie unter [Kompilieren mit dem aktuellen Compiler.](dx-graphics-tools-fxc-using.md)

## <a name="related-topics"></a>Zugehörige Themen

* [Effektcompilertool](fxc.md)
