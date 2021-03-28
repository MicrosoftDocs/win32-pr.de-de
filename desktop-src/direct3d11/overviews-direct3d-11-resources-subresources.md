---
title: Unter Berichte (Direct3D 11-Grafiken)
description: In diesem Thema werden Textur-unter Ressourcen oder Teile einer Ressource beschrieben.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039908"
---
# <a name="subresources-direct3d-11-graphics"></a>Unter Berichte (Direct3D 11-Grafiken)

In diesem Thema werden Textur-unter Ressourcen oder Teile einer Ressource beschrieben.

Direct3D kann auf eine gesamte Ressource verweisen, oder Sie kann auf Teilmengen einer Ressource verweisen. Der Begriff "subresource" verweist auf eine Teilmenge einer Ressource.

Ein Puffer ist als einzelne untergeordnete Quelle definiert. Texturen sind etwas komplizierter, da einige verschiedene Textur Typen (1D, 2D usw.) aufweisen, von denen einige MipMap-Ebenen und/oder Textur Arrays unterstützen. Beginnend mit dem einfachsten Fall wird eine 1D-Textur als einzelne untergeordnete Quelle definiert, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1D-Textur](images/d3d10-1d-texture.png)

Dies bedeutet, dass das Array von texeln, die eine 1D-Textur bilden, in einer einzelnen untergeordneten Quelle enthalten ist.

Wenn Sie eine 1D-Textur mit drei MipMap-Ebenen erweitern, kann Sie wie in der folgenden Abbildung dargestellt werden.

![Abbildung einer 1D-Textur mit drei MipMap-Ebenen](images/d3d10-resource-texture1d.png)

Stellen Sie sich dies als eine einzelne Textur vor, die aus drei unter Ressourcen besteht. Ein unter Bericht kann mit der Detailgenauigkeit (LOD) für eine einzelne Textur indiziert werden. Wenn Sie ein Array von Texturen verwenden, sind für den Zugriff auf eine bestimmte untergeordnete Quelle sowohl die Lod als auch die jeweilige Textur erforderlich. Alternativ kombiniert die API diese beiden Informationen in einem einzelnen Null basierten unter Quell Index, wie in der folgenden Abbildung dargestellt.

![Abbildung eines NULL basierten unter Quell Indexes](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a>Auswählen von unter Ressourcen

Einige APIs greifen auf eine gesamte Ressource zu (z. b. die [**Verknüpfung id3d11devicecontext aus:: copyresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) -Methode), von denen andere auf einen Teil einer Ressource zugreifen (z. b. die [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) -Methode oder die [**Verknüpfung id3d11devicecontext aus:: copysubresourceregion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) -Methode). Die Methoden, die auf einen Teil einer Ressource zugreifen, verwenden im Allgemeinen eine Ansichts Beschreibung (z. b. die [**D3D11 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) -Struktur), um die unter Ressourcen anzugeben, auf die zugegriffen werden soll.

Die Abbildungen in den folgenden Abschnitten zeigen die Begriffe, die von einer Ansichts Beschreibung beim Zugriff auf ein Array von Texturen verwendet werden.

### <a name="array-slice"></a>Array Slice

Bei einem Array von Texturen enthält jede Textur mit Mipmaps, ein *Array Slice* (dargestellt durch das weiße Rechteck), eine Textur und alle zugehörigen unter Ressourcen, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Array Slice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>MIP-Slice

Ein *MIP-Slice* (dargestellt durch das weiße Rechteck) enthält eine MipMap-Ebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.

![Abbildung eines MIP-Slice](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Auswählen einer einzelnen untergeordneten Quelle

Sie können diese beiden Arten von Slices verwenden, um eine einzelne untergeordnete Quelle auszuwählen, wie in der folgenden Abbildung dargestellt.

![Abbildung der Auswahl eines unter Berichts mithilfe eines Array Slice und eines MIP-Slice](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Auswählen mehrerer unter Ressourcen

Oder Sie können diese beiden Arten von Slices mit der Anzahl von MipMap-Ebenen und/oder der Anzahl von Texturen verwenden, um mehrere unter Ressourcen auszuwählen, wie in der folgenden Abbildung dargestellt.

![Darstellung der Auswahl mehrerer unter Berichte](images/d3d10-resource-subresources-2.png)

> [!Note]  
> Eine [**renderzielansicht**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) kann nur eine einzelne untergeordnete Quelle oder einen MIP-Slice verwenden und darf keine unter Ressourcen aus mehreren MIP-Slice enthalten. Das heißt, jede Textur in einer renderzielansicht muss dieselbe Größe aufweisen. In der [**Ansicht "Shader-Resource**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) " kann ein beliebiger rechteckiger Bereich von unter Berichten ausgewählt werden, wie in der Abbildung dargestellt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




