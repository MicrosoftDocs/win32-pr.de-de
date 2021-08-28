---
title: Kernfunktionen (Direct3D 12-Grafiken)
description: Die folgenden Funktionen werden in d3d12.h deklariert.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: e38145bc4aef4c07ba00de4185fc97ad449f4f2c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881788"
---
# <a name="core-functions"></a>Core-Funktionen

Die folgenden Funktionen werden in d3d12.h deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | Erstellt ein Gerät, das den Adapter darstellt. |
| [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | Deserialisiert eine Stammsignatur, sodass Sie die Layoutdefinition [**(D3D12 \_ ROOT \_ SIGNATURE \_ DESC) bestimmen können.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) |
| [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | Generiert eine Schnittstelle, die die deserialisierte Datenstruktur über [**GetUnconvertedRootSignatureDesc zurückgeben kann.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) |
| [**D3D12EnableExperimentalFeatures**](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | Aktiviert eine Liste experimenteller Features. |
| [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | Ruft eine Debugschnittstelle ab. |
| [**D3D12GetInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Wählt zur Laufzeit eine SDK-Version aus, wenn sich das System im Windows Befindet. |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | Serialisiert eine Stammsignaturversion 1.0, die an [**ID3D12Device::CreateRootSignature übergeben werden kann.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) |
| [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Serialisiert eine Stammsignatur einer beliebigen Version, die an [**ID3D12Device::CreateRootSignature übergeben werden kann.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) |

## <a name="related-topics"></a>Zugehörige Themen

* [Core-Referenz](direct3d-12-core-reference.md)
* [Referenz zu Direct3D 12](direct3d-12-reference.md)
