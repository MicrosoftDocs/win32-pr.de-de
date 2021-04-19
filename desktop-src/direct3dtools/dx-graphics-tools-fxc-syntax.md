---
title: Syntax
description: Hier ist die Syntax zum Aufrufen von FXC.exe, dem Effekt-Compiler-Tool. Ein Beispiel finden Sie unter Offline Kompilierung.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106337474"
---
# <a name="syntax"></a>Syntax

Hier ist die Syntax zum Aufrufen von FXC.exe, dem Effekt-Compiler-Tool. Ein Beispiel finden Sie unter [Offline Kompilierung](dx-graphics-tools-fxc-using.md).

-   [Verwendung](#usage)
-   [Argumente](#arguments)
-   [Anmerkungen](#remarks)
-   [Profiles](#profiles)
-   [Versions Hinweise](#version-notes)
-   [Zugehörige Themen](#related-topics)

## <a name="usage"></a>Verbrauch

**FXC** *switchoptions* - *Datei* Namen

## <a name="arguments"></a>Argumente
Trennen Sie jede Switch-Option durch ein Leerzeichen oder einen Doppelpunkt.

### <a name="switchoptions"></a>*Switchoptions*
\[in \] Kompilierungsoptionen. Es gibt nur eine erforderliche Option und vieles mehr, das optional ist. Trennen Sie jede durch ein Leerzeichen oder einen Doppelpunkt.

#### <a name="required-option"></a>Erforderliche Option
##### <a name="t-profile"></a>/T <*Profil*>
Shadermodell (siehe [profile](#profiles)).

#### <a name="optional-options"></a>Optionale Optionen
##### <a name="-help"></a>/?, /help
Hilfe zum Drucken von `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*Command. Option. file*>
Eine Datei, die zusätzliche Kompilierungsoptionen enthält. Diese Option kann mit anderen Kompilierungsoptionen für die Befehlszeile gemischt werden. Der *Befehl. Option. File* darf nur eine Option pro Zeile enthalten. Der *Befehl. Option. File* darf keine leeren Zeilen enthalten. Die in der Datei angegebenen Optionen dürfen keine führenden oder nachfolgenden Leerzeichen enthalten.

##### <a name="all_resources_bound"></a>/all_resources_bound
Aktivieren Sie aggressive Vereinfachung in SM 5.1 und höher. Neu für Direct3D 12.

##### <a name="cc"></a>/CC
Ausgabe Farbe codierte Assembly.

##### <a name="compress"></a>/compress
Komprimieren des DX10-Shader-Bytecode aus Dateien.

##### <a name="d-idtext"></a>/D <*ID*- >=< *Text*>
Definieren Sie das Makro.

##### <a name="decompress"></a>/decompress
Dekomprimieren von DX10-Shader-Bytecode aus der ersten Datei. Ausgabedateien müssen in der Reihenfolge aufgelistet werden, in der Sie sich während der Komprimierung befanden.

##### <a name="dumpbin"></a>/dumpbin
Lädt eine Binärdatei, anstatt einen Shader zu kompilieren.

##### <a name="e-name"></a>/E <name>
Shader-Einstiegspunkt. Wenn kein Einstiegspunkt angegeben wird, wird **Main** als Shader-Eintrags Name betrachtet.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Aktiviert ungebundene deskriptortabellen. Neu für Direct3D 12.

##### <a name="extractrootsignature-file"></a>/extractrootsignature <*Datei*>
Extrahieren Sie die Stamm Signatur aus Shader-Bytecode. Neu für Direct3D 12.

##### <a name="fc-file"></a>/FC <*Datei*>
Ausgabeassembly-Codelisten Datei.

##### <a name="fd-file"></a>/FD <*Datei*>
Extrahieren Sie die Informationen der Shader-Programmdatenbank (PDB), und schreiben Sie Sie in die angegebene Datei. Wenn Sie den Shader kompilieren, verwenden Sie/FD, um eine PDB-Datei mit shaderdebuginformationen zu generieren.

##### <a name="fe-file"></a>/FE <*Datei*>
Gibt Warnungen und Fehler in der angegebenen Datei aus.

##### <a name="fh-file"></a>/FH <*Datei*>
Ausgabe Header Datei, die den Objektcode enthält.

##### <a name="fl-file"></a>/FL <*Datei*
Gibt eine Bibliothek aus. Erfordert den D3dcompiler- \_47.dll oder eine spätere Version der dll.

##### <a name="fo-file"></a>/FO <*Datei*>
Ausgabe Objektdatei. Häufig wird die Erweiterung &quot; . FXC &quot; verwendet, obwohl andere Erweiterungen verwendet werden, wie z &quot; . b.. o &quot; , &quot; . obj &quot; oder &quot; . dxbc &quot; .

##### <a name="fx-file"></a>/FX <*Datei*>
Ausgabeassemblycode und Hex-Listen Datei

##### <a name="gch"></a>/Gch
Als untergeordneten Effekt für fx_4_x profile kompilieren.

> [!NOTE]
> Die Unterstützung für Legacy Effekt Profile ist veraltet.

##### <a name="gdp"></a>/Gdp
Deaktivieren Sie den Leistungsmodus des Effekts.

##### <a name="gec"></a>/Gec
Aktivieren Sie den abwärts Kompatibilitätsmodus.

##### <a name="ges"></a>/Ges
Aktivieren Sie den Strict-Modus.

##### <a name="getprivate-file"></a>/getprivate <*Datei*>
Speichert private Daten aus dem Shader-BLOB (kompilierte Shader-Binärdatei) in der angegebenen Datei. Extrahiert private Daten, die zuvor durch/setprivate eingebettet wurden, aus dem Shader-BLOB.

Sie müssen die/dumpbin-Option mit/getprivate. angeben. Beispiel:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Vermeiden Sie flowsteuerungskonstrukte.

##### <a name="gfp"></a>/GFP
Flow-steuerungskonstrukte bevorzugen.

##### <a name="gis"></a>/Gis
Erzwingen der IEEE-strenge.

##### <a name="gpp"></a>/Gpp
Partielle Genauigkeit erzwingen.
    
##### <a name="i-include"></a>/I <*einschließen*>
Zusätzlicher Include-Pfad.

##### <a name="lx"></a>/Lx
Ausgabe hexadezimal Literale. Erfordert den D3dcompiler- \_47.dll oder eine spätere Version der dll.

##### <a name="matchuavs"></a>/matchUAVs
Entsprechung für Vorlagen-Shader-UAV-Slot-Zuweisungen im aktuellen Shader. Weitere Informationen finden Sie unter " <a href="#remarks">Hinweise</a>".

##### <a name="mergeuavs"></a>/mergeUAVs
UAV-Slot-Zuordnungen von Vorlagen-Shader und dem aktuellen Shader zusammenführen. Weitere Informationen finden Sie unter " <a href=""></a> <a href="#remarks">Hinweise</a>".

##### <a name="ni"></a>/Ni
Ausgabe Anweisungs Nummern in assemblyauflistungen.

##### <a name="no"></a>/No
Byte Offset der Ausgabe Anweisung in Assemblylisten. Wenn Sie eine Assembly entwickeln, verwenden Sie/No, um Sie mit dem Byte Offset für jede Anweisung zu kommentieren.

##### <a name="nologo"></a>/nologo
Copyrightmeldung unterdrücken

##### <a name="od"></a>/Od
Deaktiviert Optimierungen. /Od impliziert/GFP, aber die Ausgabe ist möglicherweise nicht identisch mit/od/GFP.

##### <a name="op"></a>/Op
Deaktivieren Sie preshaders (veraltet).

##### <a name="o0-o1-o2-o3"></a>/O0/O1,/O2,/O3
Optimierungs Ebenen. O1 ist die Standardeinstellung.
- O0: deaktiviert die Neuanordnung von Anweisungen. Dies trägt zur Verringerung der Register Last bei und ermöglicht eine schnellere Schleifen Simulation.
- O1: deaktiviert die Neuanordnen der Anweisung für ps_3_0 und aufwärts.
- O2-identisch mit O1. Für die zukünftige Verwendung reserviert.
- O3-identisch mit O1. Für die zukünftige Verwendung reserviert.

##### <a name="p-file"></a>/P <*Datei*>
In Datei Vorverarbeiten (muss alleine verwendet werden).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Entfernen Sie Debugdaten aus Shader-Bytecode für 4_0 +-Profile.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Entfernen Sie die privaten Daten aus 4_0 + Shader-Bytecode. Entfernt private Daten (beliebige Bytefolge) aus dem Shader-BLOB (kompilierter Shader-Binärdatei), die Sie zuvor mit der Option eingebettet haben `/setprivate <file>` .

Sie müssen die/dumpbin-Option mit/Qstrip_priv angeben. Beispiel:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Entfernen Sie reflektionsdaten aus Shader-Bytecode für 4_0 +-Profile.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Stamm Signatur aus Shader-Bytecode entfernen. Neu für Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Angenommen, UAVs/Srvs können für cs_5_0 + Alias Alias sein. Erfordert den D3dcompiler- \_47.dll oder eine spätere Version der dll.

##### <a name="setprivate-file"></a>/setprivate <*Datei*>
Fügen Sie dem kompilierten Shader-BLOB private Daten in der angegebenen Datei hinzu. Bettet die angegebene Datei, die als rohpuffer behandelt wird, in das Shader-BLOB ein. Verwenden Sie/setprivate, um beim Kompilieren eines Shaders private Daten hinzuzufügen. Sie können auch die/dumpbin-Option mit/setprivate verwenden, um ein vorhandenes Shader-Objekt zu laden, und nachdem sich das Objekt im Arbeitsspeicher befindet, um das private dateiblob hinzuzufügen. Verwenden Sie z. b. entweder einen einzelnen Befehl mit/setprivate, um einem kompilierten Shader-BLOB private Daten hinzuzufügen:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
Oder verwenden Sie zwei Befehle, bei denen der zweite Befehl ein Shader-Objekt lädt und dann private Daten hinzufügt:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>/setrootsignature <*Datei*>
Fügt die Stammsignatur an Shader-Bytecode an. Neu für Direct3D 12.

##### <a name="shtemplate-file"></a>/shtemplate <*Datei*>
Verwenden Sie die angegebene Vorlagen-shaderdatei zum Zusammenführen (/mergeUAVs) und zum Abgleichen von (/matchUAVs) Ressourcen. Weitere Informationen finden Sie unter " <a href="#remarks">Hinweise</a>".

##### <a name="vd"></a>/VD
Deaktivieren Sie die Validierung.

##### <a name="verifyrootsignature-file"></a>/verifyrootsignature <*Datei*>
Überprüfen Sie den Shader-Bytecode anhand der Stamm Signatur. Neu für Direct3D 12.

##### <a name="vi"></a>/Vi
Zeigt Details zum include-Prozess an.

##### <a name="vn-name"></a>/VN <*Name*>
Verwenden Sie den Namen als Variablennamen in der Header Datei.

##### <a name="wx"></a>/WX
Behandeln Sie Warnungen als Fehler.

##### <a name="zi"></a>/ZI
Aktiviert Debuginformationen.

##### <a name="zpc"></a>/Zpc
Paket Matrizen in der Spalte-Haupt Reihenfolge.

##### <a name="zpr"></a>/Zpr
Paket Matrizen in Zeilen-Haupt Reihenfolge.

### <a name="filenames"></a>*Dateinamen*

\[in \] den Dateien, die die Shader (s) und/oder die Auswirkung (e) enthalten.

## <a name="remarks"></a>Bemerkungen

Verwenden `/mergeUAVs` Sie die `/matchUAVs` Optionen, und `/shtemplate` , um die UAV-Bindungs Slots für eine Kette von Shadern auszurichten.

Angenommen, Sie verfügen über Shader A. FX, B. FX und C. fx. Um die UAV-Bindungs Slots für diese Kette von Shader auszurichten, benötigen Sie zwei durch Führungen der Kompilierung:

**So richten Sie die UAV-Bindungs Slots für eine Kette von Shadern aus**

1.  Verwenden Sie/mergeUAVs, um Shader zu kompilieren, und geben Sie ein zuvor kompiliertes Shader-BLOB mit/shtemplate. an. Beispiel:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Verwenden Sie/matchUAVs, um Shader zu kompilieren, und geben Sie das letzte Shader-BLOB aus dem ersten Durchlauf mit/shtemplate. an. Sie können in beliebiger Reihenfolge kompilieren. Beispiel:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
C. FX muss im zweiten Durchlauf nicht neu kompiliert werden.

Nachdem Sie die vorherigen beiden Kompilierungs Durchläufen durchgeführt haben, können Sie A. o, B. o und C. o als abschließende Shader-BLOBs mit ausgerichteten UAV-Slots verwenden.

## <a name="profiles"></a>Profiles

Jedes Shader-Modell wird mit einem HLSL-Profil bezeichnet. Um einen Shader für ein bestimmtes Shader-Modell zu kompilieren, wählen Sie das entsprechende Shader-Profil aus der folgenden Tabelle aus.

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
</dl></td></tr><tr class="even"><td>HLSL-Shader-Verknüpfung </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Weitere Informationen zum Verknüpfen von Shader finden Sie unter <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> und <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>. <br/></td></tr><tr class="odd"><td>Rumpf-Shader</td><td><dl> hs_5_0<br />
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
</dl></td></tr><tr class="odd"><td>Stamm Signatur</td><td><dl> rootsig_1_0<br />
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

## <a name="version-notes"></a>Versions Hinweise

Direct3D 12 finden Sie unter [Angeben von Stamm Signaturen in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Ressourcen Bindung in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) und [dynamischer Indizierung mit HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).

Verwenden Sie in Direct3D 10 die API, um das Vertex-, Geometrie-und Pixel-Shader-Profil zu erhalten, das für ein bestimmtes Gerät am besten geeignet ist, indem Sie die folgenden Funktionen aufrufen: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)und [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

In Direct3D 9 verwenden Sie die [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) -Methode oder die [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) -Methode, um die von einem Gerät unterstützten Scheitelpunkt-und Pixel-Shader-Profile abzurufen. Die von diesen Methoden zurückgegebene [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) -Struktur gibt die Vertex-und Pixel-Shader-Profile an, die von einem Gerät in seinen **VertexShaderVersion** -und **PixelShaderVersion** -Membern unterstützt werden

Beispiele finden Sie unter [Kompilieren mit dem aktuellen Compiler](dx-graphics-tools-fxc-using.md).

## <a name="related-topics"></a>Zugehörige Themen

* [Effekt-Compilertool](fxc.md)