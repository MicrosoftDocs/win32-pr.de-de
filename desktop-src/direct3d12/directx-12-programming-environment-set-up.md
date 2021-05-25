---
title: Einrichtung der Direct3D 12 Programmierungsumgebung
description: Beschreibt die Installation, Tools und unterstützten Bibliotheken, die eine produktive Direct3D 12-Entwicklungsumgebung darstellen.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7079207f91185cc14b37d9056a4fa813b251bce5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342815"
---
# <a name="direct3d-12-programming-environment-setup"></a>Einrichtung der Direct3D 12 Programmierungsumgebung

Beschreibt die Installation, Tools und unterstützten Bibliotheken, die eine produktive Direct3D 12-Entwicklungsumgebung darstellen.

-   [Entwicklungsumgebung](#development-environment)
-   [Unterstützte Sprachen](#supported-languages)
-   [Hilfsstrukturen](#helper-structures)
-   [Speicherverwaltungsbibliothek](#memory-management-library)
-   [Unterstützte Tools und Bibliotheken](#supported-tools-and-libraries)
-   [Beispiele](#samples)
-   [Debugebene](#debug-layer)
-   [Videos zu Bildungseinrichtungen](#educational-videos)
-   [Verwandte Themen](#related-topics)

## <a name="development-environment"></a>Entwicklungsumgebung

Die Direct3D 12-Header und -Bibliotheken sind Teil des Windows 10 SDK. Für die Verwendung von Direct3D 12 ist kein separater Download oder keine separate Installation erforderlich.

Nachdem Sie die Windows 10 SDK-Software und Visual Studio installiert haben, ist das Setup Ihrer Direct3D 12-Programmierumgebung abgeschlossen. Visual Studio 2019 wird empfohlen, da es die D3D12-Grafikdebuggingtools enthält, frühere Versionen von Visual Studio jedoch für die Programmentwicklung funktionieren.

Um die [Direct3D 12-API](direct3d-12-reference.md)zu verwenden, schließen Sie D3d12.h ein, und verknüpfen Sie D3d12.lib, oder fragen Sie die Einstiegspunkte direkt in D3d12.dll.

Die folgenden Header und Bibliotheken sind verfügbar. Der Speicherort der statischen Bibliotheken hängt von der Version (32-Bit oder 64-Bit) der Windows 10, die auf Ihrem Computer ausgeführt wird.



| Name der Header- oder Bibliotheksdatei | BESCHREIBUNG                         | Installationsverzeichnis      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12.h                     | Direct3D 12-API-Header              | %WindowsSdkDir \\ Include \% WindowsSDKVersion% \\ \um |
| D3d12.lib                   | Statische Direct3D 12-API-Stubbibliothek | %WindowsSdkDir \\ Lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Dynamische Direct3D 12-API-Bibliothek     | %WINDIR% \\ System32    |
| D3d12SDKLayers.h            | Direct3D 12-Debugheader            | %WindowsSdkDir \\ Include \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Dynamische Direct3D 12-Debugbibliothek   | %WINDIR% \\ System32    |



## <a name="supported-languages"></a>Unterstützte Sprachen

C++ ist die einzige unterstützte Sprache für die Direct3D 12-Entwicklung, C# und andere .NET-Sprachen werden nicht unterstützt.

## <a name="helper-structures"></a>Hilfsstrukturen

Es gibt eine Reihe von Hilfsstrukturen, die insbesondere das Initialisieren einer Reihe von D3D12-Strukturen erleichtern. Diese Strukturen und einige Hilfsfunktionen befinden sich im Header D3dx12.h. Dieser Header ist Open Source und kann von einem Entwickler nach Bedarf geändert werden. Laden Sie ihn von [der D3D12-Hilfsbibliothek](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) herunter, und lesen Sie [Helper Structures and Functions for D3D12 (Hilfsstrukturen und Funktionen für D3D12).](helper-structures-and-functions-for-d3d12.md)

## <a name="memory-management-library"></a>Speicherverwaltungsbibliothek

Eine Hilfsbibliothek für die Speicherverwaltung steht zum Download zur Verfügung, die Sie in Ihre App integrieren können, um das D3D11-Speicherverwaltungsverhalten besser zu berücksichtigen. Als D3D11-Stilverwaltungsbibliothek ist sie am effektivsten bei Apps, die weiterhin eine Strategie für die Zuordnung von Ressourcenstilen verwenden, für die ein *Commit ausgeführt* wurde. Insbesondere sollte die Bibliothek als schrittweiser Schritt angesehen werden, der Ihnen den größten Teil des Wegs zurück zur leistungsorientierten D3D11-Speicherverwaltung ermöglicht, wenn sie in Szenarien mit eingeschränktem Arbeitsspeicher (z. B. Low-End-Arbeitsspeicherkarten, 4K, Ultra-Einstellungen usw.) verwendet wird. D3D12-APIs ermöglichen Techniken, mit denen Sie eine noch bessere Speichereffizienz als D3D11 erzielen können, obwohl diese Techniken schwierig und zeitaufwändig sein können.

Beachten Sie, dass diese Bibliothek gerade ausgeführt wird und sich im Laufe der Zeit ändern kann. Verwenden Sie die unten angegebenen Links, um auf die Bibliothek und Beispiele zuzugreifen.

-   [The D3D12 Residency Starter Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Unterstützte Tools und Bibliotheken

Die folgenden Bibliotheken können alle mit Direct3D 12 verwendet werden.



| Bibliothek                                                                                 |  Zweck                                                                                                                                                                                                                                                                      | Dokumentation                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [DirectX Tool Kit für DirectX 12](https://github.com/Microsoft/DirectXTK12) | Eine umfangreiche Sammlung von Hilfsklassen zum Schreiben von Direct3D 12 C++-Code für Universelle Windows-Plattform-Apps (UWP), Win32-Desktopanwendungen für Windows 10 und Xbox One exklusiven Apps.                                                                         | [DirectX12TK-Wiki](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Verwenden Sie dies zum Lesen und Schreiben von DDS-Dateien sowie zum Ausführen verschiedener Verarbeitungsvorgänge für Texturinhalte, z. B. Größenänderung, Formatkonvertierung, MIP-Kartengenerierung, Blockkomprimierung für Texturressourcen der Direct3D-Laufzeit und Höhenzuordnung in normale Kartenkonvertierung. | [DirectXTex-Wiki](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Verwenden Sie diese Methode, um verschiedene Verarbeitungsvorgänge für Geometrieinhalte auszuführen, z. B. das Generieren von Normalitäten und Tangentenrahmen, Berechnungen der Dreiecksadjaz und die Optimierung des Scheitelpunktcaches.                                                                                | [DirectXMesh-Wiki](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Eine große Anzahl von Hilfsklassen und -methoden zur Unterstützung von Vektoren, Skalaren, Matrizen, Quaternionen und vielen anderen mathematischen Operationen.                                                                                                                               | [DirectXMath-Dokumentation auf MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Verwenden Sie dies zum Erstellen und Packen eines Isocharttexturat atlas.                                                                                                                                                                                                           | [UVAtlas wiki](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Beispiele

Eine Liste der funktionierenden D3D12-Beispiele und deren Suche und Ausführung finden Sie unter [Working Samples](working-samples.md).

Exemplarische Vorgehensweisen zum Hinzufügen von Code zum Aktivieren bestimmter Features finden Sie unter [Exemplarische Vorgehensweisen für D3D12-Code.](d3d12-code-walk-throughs.md)

## <a name="debug-layer"></a>Debugebene

Die Debugebene bietet eine umfassende zusätzliche Parameter- und Konsistenzüberprüfung (z. B. Überprüfen der Shaderbindung und Ressourcenbindung, Überprüfen der Parameterkonsistenz und Melden von Fehlerbeschreibungen).

> [!Note]  
> Um Windows 10 ein Gerät zu erstellen, das die Debugebene unterstützt, aktivieren Sie das optionale Feature "Grafiktools". Wechseln Sie zum Bereich Einstellungen unter System, Apps & Features, Optionale Features verwalten, Feature hinzufügen, und suchen Sie dann nach "Grafiktools".

Der Header, der zur Unterstützung der Debugebene D3D12SDKLayers.h erforderlich ist, ist standardmäßig in d3d12.h enthalten.

Wenn die Debugebene Speicherverluste auflistet, gibt sie eine Liste von Objektschnittstellenzeigern zusammen mit ihren Anzeigenamen aus. Der Standardmäßige Anzeigename ist &lt; "unbenannt". &gt; Sie können den Anzeigenamen mithilfe der [**ID3D12Object::SetName-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) festlegen. In der Regel sollten Sie diese Aufrufe aus Ihrer Produktionsversion kompilieren.

Es wird empfohlen, die Debugebene zu verwenden, um Ihre Apps zu debuggen, um sicherzustellen, dass sie von Fehlern und Warnungen bereinigt werden. Die Debugebene unterstützt Sie beim Schreiben von Direct3D 12-Code. Darüber hinaus kann Ihre Produktivität bei Verwendung der Debugebene gesteigert werden, da Sie sofort die Ursachen für obskure Renderingfehler oder sogar schwarze Bildschirme an der Quelle sehen können. Die Debugebene stellt Warnungen für viele Probleme bereit. Beispiel:

-   Vergessen Sie, eine Textur festzulegen, aber in Ihrem Pixel-Shader aus ihr zu lesen.
-   Ausgabetiefe, aber keine Begrenzung des Tiefenschablonenzustands.
-   Fehler bei der Texturerstellung mit INVALIDARG.

Legen Sie fest, dass der Compiler D3DCOMPILE \_ DEBUG definiert, um den HLSL-Compiler an weist, Debuginformationen in das Shaderblob einzuschließen.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Ausführliche Informationen zu allen Debugschnittstellen und -methoden finden Sie in der Referenz zur [Debugebene.](direct3d-12-sdklayers-reference.md)

Übersichtsinformationen zur Verwendung der Debugebene finden Sie unter Grundlegendes zur [D3D12-Debugebene.](understanding-the-d3d12-debug-layer.md)

## <a name="educational-videos"></a>Schulungsvideos

Es gibt eine Reihe von Videos zu Direct3D 12 und Windows 10 in [den Videotutorials](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)für erweitertes Lernen von DirectX, einschließlich Videos zu Grafikdebuggingtools und Melden von Grafikfehlern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 