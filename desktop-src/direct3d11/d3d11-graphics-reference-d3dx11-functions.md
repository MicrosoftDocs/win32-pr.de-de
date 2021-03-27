---
title: D3DX-Funktionen (Direct3D 11-Grafiken)
description: Dieser Abschnitt enthält Informationen zu den Funktionen von D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- Functions, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391350"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a>D3DX-Funktionen (Direct3D 11-Grafiken)

Dieser Abschnitt enthält Informationen zu den Funktionen von D3DX 11.

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 


## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> -API verwenden.
</blockquote>
<br/> Kompilieren Sie einen Shader oder einen Effekt aus einer Datei.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> -API verwenden.
</blockquote>
<br/> Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden und dann mithilfe des Befehlszeilen Compilers von Fxc.exe offline zu kompilieren oder eine der HLSL-Kompilierungs-APIs wie die <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> -API zu verwenden.
</blockquote>
<br/> Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek " <strong>computenormalmap</strong>" zu verwenden.
</blockquote>
<br/> Konvertiert eine Höhen Zuordnung in eine normale Karte. Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen eines asynchronen Daten Prozessors für einen Shader.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie ein asynchrones Datei Lade Modul.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie ein Lade Modul für asynchrone Speicher.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie ein asynchrones Ressourcen Lade Modul.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie einen Datenprozessor für einen Shader asynchron.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie einen Datenprozessor, der mit einem <a href="id3dx11threadpump.md"><strong>threadpump</strong></a>verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie einen Datenprozessor, der mit einem <a href="id3dx11threadpump.md"><strong>threadpump</strong></a>verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür. Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in Bibliothek d3dx11, die <a href="id3dx11threadpump.md"><strong>Thread-Pumpen</strong></a>verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> -Bibliothek (Laufzeit), " <strong>kreatexxxtexturefromfile</strong> " (wobei xxx DDS oder WIC ist)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxfile</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreateshaderresourceview</strong> "</li>
</ul>
</blockquote>
<br/> Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreateshaderresourceview</strong> "</li>
</ul>
</blockquote>
<br/> Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden, die dann folgende Aktionen ausführen:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreateshaderresourceview</strong> "</li>
</ul>
</blockquote>
<br/> Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Ressource.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> -Bibliothek (Laufzeit), " <strong>kreatexxxtexturefromfile</strong> " (wobei xxx DDS oder WIC ist)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxfile</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreatetexture</strong> "</li>
</ul>
</blockquote>
<br/> Erstellen Sie eine Textur Ressource aus einer Datei.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreatetexture</strong> "</li>
</ul>
</blockquote>
<br/> Erstellen Sie eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden, die dann folgende Aktionen ausführen:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreatetexture</strong> "</li>
</ul>
</blockquote>
<br/> Erstellen Sie eine Textur aus einer anderen Ressource.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Siehe Hinweise.
</blockquote>
<br/> Erstellen Sie ein Thread-Pump.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek, <strong>generatemipmaps</strong> und <strong>GenerateMipMaps3D</strong>verwenden.
</blockquote>
<br/> Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>GetMetadataFromXXXFile</strong> (wobei xxx für WIC, DDS oder TGA verwendet wird) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).
</blockquote>
<br/> Ruft Informationen zu einer angegebenen Bilddatei ab.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>GetMetadataFromXXXMemory</strong> (wobei xxx für WIC, DDS oder TGA verwendet wird) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).
</blockquote>
<br/> Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden und anschließend die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (wobei xxx für WIC, DDS oder TGA steht) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).
</blockquote>
<br/> Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek zu verwenden, die <strong>Größe zu ändern</strong>, zu <strong>konvertieren</strong>, zu <strong>komprimieren</strong>, zu <strong>dekomprimieren</strong>und/oder <strong>copyrechteck</strong>.
</blockquote>
<br/> Lädt eine Textur aus einer Textur.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> -API zu verwenden.
</blockquote>
<br/> Erstellen Sie einen Shader aus einer Datei, ohne ihn zu kompilieren.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> -API zu verwenden.
</blockquote>
<br/> Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> -API zu verwenden.
</blockquote>
<br/> Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>capturetexture</strong> und <strong>savetoxxxfile</strong> verwenden (wobei xxx gleich WIC, DDS oder TGA ist). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer renderzieltextur empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTK">directxtk</a> -Bibliothek " <strong>saveddstexturedefile</strong> " oder " <strong>savewictexturedefile</strong>" zu verwenden.
</blockquote>
<br/> Speichert eine Textur in einer Datei.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>capturetexture</strong> , dann <strong>savetoxxxmemory</strong> (xxx ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).
</blockquote>
<br/> Speichert eine Textur im Speicher.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die für die <strong>spprojectcubemap</strong>verwendete <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">sphärischen Harmonics</a> -Bibliothek zu verwenden.
</blockquote>
<br/> Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>Verknüpfung id3d11devicecontext aus:: clearstate</strong></a> -Methode zu verwenden.
</blockquote>
<br/> Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf <strong>null</strong>festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

