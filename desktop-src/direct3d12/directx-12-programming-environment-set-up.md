---
title: Einrichtung der Direct3D 12 Programmierungsumgebung
description: Beschreibt die Installation, Tools und unterstützten Bibliotheken, die eine produktive Direct3D 12-Entwicklungsumgebung bilden.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e6af0d0a93d55f700478ec839f3864ee0efbcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548747"
---
# <a name="direct3d-12-programming-environment-setup"></a>Einrichtung der Direct3D 12 Programmierungsumgebung

Beschreibt die Installation, Tools und unterstützten Bibliotheken, die eine produktive Direct3D 12-Entwicklungsumgebung bilden.

-   [Entwicklungsumgebung](#development-environment)
-   [Unterstützte Sprachen](#supported-languages)
-   [Hilfsstrukturen](#helper-structures)
-   [Speicher Verwaltungs Bibliothek](#memory-management-library)
-   [Unterstützte Tools und Bibliotheken](#supported-tools-and-libraries)
-   [Beispiele](#samples)
-   [Ebene Debuggen](#debug-layer)
-   [Schulungsvideos](#educational-videos)
-   [Verwandte Themen](#related-topics)

## <a name="development-environment"></a>Entwicklungsumgebung

Die Direct3D 12-Header und-Bibliotheken sind Teil des Windows 10-SDK. Für die Verwendung von Direct3D 12 ist kein separater Download oder eine separate Installation erforderlich.

Nachdem Sie die Windows 10 SDK-Software und Visual Studio installiert haben, ist die Einrichtung ihrer Direct3D 12-Programmierumgebung fertiggestellt. Visual Studio 2019 wird empfohlen, da es die Tools zum Debuggen von D3D12-Grafiken enthält, aber frühere Versionen von Visual Studio für die Programmentwicklung funktionieren.

Um die [Direct3D 12-API](direct3d-12-reference.md)zu verwenden, schließen Sie D3d12. h ein, und verknüpfen Sie Sie mit D3d12. lib, oder Fragen Sie die Einstiegspunkte direkt in D3d12.dll ab.

Die folgenden Header und Bibliotheken sind verfügbar. Der Speicherort der statischen Bibliotheken hängt von der Version (32-Bit oder 64-Bit) von Windows 10 ab, die auf Ihrem Computer ausgeführt wird.



| Header-oder Bibliotheks Dateiname | Beschreibung                         | Installationsverzeichnis      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12. h                     | Direct3D 12-API-Header              | % WindowsSdkDir \\ include \% windowssdkversion% \\ \Um |
| D3d12. lib                   | Statische Direct3D 12-API-Stub-Bibliothek | % WindowsSdkDir \\ lib \% windowssdkversion% \\ \en\arch |
| D3d12.dll                   | Dynamic Direct3D 12-API-Bibliothek     | % Windir% \\ system32    |
| D3d12SDKLayers. h            | Direct3D 12-Debug-Header            | % WindowsSdkDir \\ include \% windowssdkversion% \\ \Um |
| D3d12SDKLayers.dll          | Dynamic Direct3D 12-Debugbibliothek   | % Windir% \\ system32    |



## <a name="supported-languages"></a>Unterstützte Sprachen

C++ ist die einzige unterstützte Sprache für Direct3D 12-Entwicklung, c# und andere .NET-Sprachen werden nicht unterstützt.

## <a name="helper-structures"></a>Hilfsstrukturen

Es gibt eine Reihe von Hilfsstrukturen, die die Initialisierung einer Reihe von D3D12-Strukturen erleichtern. Diese Strukturen und einige Hilfsprogrammfunktionen befinden sich im Header D3dx12. h. Dieser Header ist Open Source und kann von einem Entwickler nach Bedarf geändert werden. Laden Sie ihn aus [der D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) herunter, und verweisen Sie auf die [Hilfsstrukturen und-Funktionen für D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="memory-management-library"></a>Speicher Verwaltungs Bibliothek

Eine Hilfsbibliothek für die Speicherverwaltung steht zum Herunterladen zur Verfügung, die Sie in Ihre APP integrieren können, um das Verhalten der D3D11-Speicherverwaltung genauer abzugleichen. Als D3D11-Verwaltungs Bibliothek ist es am effektivsten bei apps, die noch eine *zugesicherte Ressourcen* Stil-Zuordnungs Strategie verwenden. Insbesondere sollte die Bibliothek als Schritt Stein betrachtet werden, der Ihnen den größten Teil der D3D11-leistungsfähigen Speicherverwaltung bietet, wenn Sie in Speicher eingeschränkten Szenarien (z. b. Low-End-Speicherkarten, 4K, ultraeinstellungen usw.) verwendet werden. D3D12-APIs aktivieren Techniken, mit denen Sie eine noch bessere Arbeitsspeicher Effizienz gegenüber D3D11 erzielen können. diese Verfahren können jedoch schwierig und zeitaufwändig zu implementieren sein.

Beachten Sie, dass diese Bibliothek gerade in Bearbeitung ist und sich im Laufe der Zeit ändern kann. Verwenden Sie die folgenden Links, um auf die Bibliothek und Beispiele zuzugreifen.

-   [Die D3D12 Residency-Starter Bibliothek](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Unterstützte Tools und Bibliotheken

Die folgenden Bibliotheken können alle mit Direct3D 12 verwendet werden.



|                                                                                  |                                                                                                                                                                                                                                                                        |                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Bibliothek**                                                                      | **Zweck**                                                                                                                                                                                                                                                            | **Dokumentation**                                                                                          |
| [DirectX-Toolkit für DirectX 12](https://github.com/Microsoft/DirectXTK12) | Eine umfangreiche Sammlung von Hilfsklassen zum Schreiben von Direct3D 12 C++-Code für universelle Windows-Plattform-Apps (UWP), Win32-Desktop Anwendungen für Windows 10 und exklusive Xbox One-apps.                                                                         | [DirectX12TK-wiki](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Verwenden Sie diese Informationen zum Lesen und Schreiben von DDS-Dateien und zum Durchführen verschiedener Vorgänge zur Verarbeitung von Textur Inhalten, einschließlich der Größenänderung, Formatkonvertierung, MIP-Map-Generierung, Block Komprimierung für Direct3D-Lauf Zeit Textur Ressourcen und Height-Map zur normalen Karten Konvertierung. | [Directxtex-wiki](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Verwenden Sie diese Option, um verschiedene Vorgänge zur Verarbeitung von Geometrie Inhalten auszuführen, z. b. das Erstellen von normalen und Tangenten Frames, Berechnungen von Dreiecks Anomalien und Vertex-Cache Optimierung.                                                                                | [Directxmesh-wiki](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Eine große Anzahl von Hilfsklassen und Methoden zur Unterstützung von Vektoren, skalaren, Matrizen, Quaternionen und vielen anderen mathematischen Vorgängen.                                                                                                                               | [Directxmath-Dokumentation auf MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Verwenden Sie diese Informationen zum Erstellen und packen eines isochart-Textur Atlas.                                                                                                                                                                                                           | [Uvatlas wiki](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Proben

Eine Liste der funktionierenden D3D12-Beispiele sowie Informationen dazu, wie Sie diese suchen und ausführen, finden Sie unter [funktionierende Beispiele](working-samples.md).

Exemplarische Vorgehensweisen zum Hinzufügen von Code, um bestimmte Funktionen zu aktivieren, finden Sie unter [D3D12 Code Walkthrough](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Ebene Debuggen

Die Debug-Ebene bietet umfassende zusätzliche Parameter-und Konsistenz Validierung (z. b. das Überprüfen der shaderverknüpfung und Ressourcen Bindung, das Überprüfen der Parameter Konsistenz und das Melden von Fehlerbeschreibungen).

> [!Note]  
> Aktivieren Sie für Windows 10 das optionale Feature "Graphics Tools", um ein Gerät zu erstellen, das die debugschicht unterstützt. Wechseln Sie zum Bereich "Einstellungen" unter "System", "Apps & Features", "optionale Features verwalten", "Features hinzufügen", und suchen Sie nach "Grafik Tools".

Der zur Unterstützung der debugschicht erforderliche Header, D3D12SDKLayers. h, ist standardmäßig in d3d12. h enthalten.

Wenn die debugschicht Speicher Verluste auflistet, gibt Sie eine Liste von Objekt Schnittstellen Zeigern zusammen mit ihren anzeigen Amen aus. Der standardmäßige Anzeige Name ist " &lt; unbenannt &gt; ". Sie können den anzeigen Amen mithilfe der [**ID3D12Object:: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) -Methode festlegen. In der Regel sollten Sie diese Aufrufe aus der Produktionsversion kompilieren.

Es wird empfohlen, dass Sie die Debugebene verwenden, um Ihre apps zu debuggen, um sicherzustellen, dass Sie Fehler und Warnungen bereinigen. Die Debug-Ebene hilft Ihnen, Direct3D 12-Code zu schreiben. Außerdem kann sich die Produktivität erhöhen, wenn Sie die debugschicht verwenden, da Sie sofort die Ursache für Fehler beim Rendern oder sogar schwarze Bildschirme an ihrer Quelle sehen können. Die Debug-Ebene bietet Warnungen für viele Probleme. Beispiel:

-   Vergessen Sie nicht, eine Textur festzulegen, sondern Sie in Ihrem Pixelshader zu lesen.
-   Ausgabe Tiefe, aber keine tiefen Schablone gebunden ist.
-   Fehler beim Erstellen der Textur mit invalidArg.

Legen Sie den Compiler define D3DCOMPILE \_ Debug fest, um dem HLSL-Compiler mitzuteilen, dass Debuginformationen in das Shader-BLOB eingeschlossen werden sollen.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Ausführliche Informationen zu allen Debugschnittstellen und-Methoden finden Sie in der [Debug-Ebenenreferenz](direct3d-12-sdklayers-reference.md).

Eine Übersicht über die Verwendung der debugschicht finden Sie Untergrund Legendes zur [D3D12 Debug-Ebene](understanding-the-d3d12-debug-layer.md).

## <a name="educational-videos"></a>Schulungsvideos

In den [Video Lernprogrammen für DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)finden Sie eine Reihe von Direct3D 12-und Windows 10-bezogenen Videos, einschließlich Videos zu Grafik-Debuggingtools und melden von Grafik Fehlern.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 