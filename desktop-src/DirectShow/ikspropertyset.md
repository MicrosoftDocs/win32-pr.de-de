---
description: Die-Schnittstelle von "ikspropertyset" wurde ursprünglich als effiziente Methode zum Festlegen und Abrufen von Geräteeigenschaften für WDM-Treiber entwickelt. dabei wurde ksproxy verwendet, um die com-Methodenaufrufe im Benutzermodus in die Kernel Modus-Eigenschaften Sätze zu übersetzen, die von WDM-Streaming-Klassen Treibern Diese Schnittstelle wird jetzt auch verwendet, um Informationen genau zwischen Softwarekomponenten zu übergeben. In einigen Fällen müssen Softwarekomponenten diese Schnittstelle oder andernfalls die "ikscontrol"-Schnittstelle implementieren (im DirectShow-DDK dokumentiert). Wenn Sie z. b. einen Software-MPEG-2-Decoder für die Verwendung mit dem DVD-Navigator schreiben, müssen Sie eine dieser Schnittstellen implementieren und außerdem die DVD-bezogenen Eigenschaften Sätze unterstützen, die der Navigator an den Decoder sendet. Pins können eine dieser Schnittstellen unterstützen, damit andere Pins oder Filter Ihre Eigenschaften festlegen oder abrufen können. Beachten Sie, dass in der DSound. h-Header Datei eine andere Schnittstelle mit diesem Namen vorhanden ist. Die beiden Schnittstellen sind nicht kompatibel. Die im DirectShow-DDK dokumentierte "ikscontrol"-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: "' Ikspropertyset '-Schnittstelle (ksproxy. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480771"
---
# <a name="ikspropertyset-interface"></a>"Ikspropertyset"-Schnittstelle

Die `IKsPropertySet` -Schnittstelle wurde ursprünglich als effiziente Methode zum Festlegen und Abrufen von Geräteeigenschaften für WDM-Treiber entwickelt. dabei wurde ksproxy verwendet, um die com-Methodenaufrufe im Benutzermodus in die Kernel Modus-Eigenschaften Sätze zu übersetzen, die von WDM-Streaming-Klassen Treibern verwendet werden. Diese Schnittstelle wird jetzt auch verwendet, um Informationen genau zwischen Softwarekomponenten zu übergeben.

In einigen Fällen müssen Softwarekomponenten diese Schnittstelle oder andernfalls die " **ikscontrol** "-Schnittstelle implementieren (im DirectShow-DDK dokumentiert). Wenn Sie z. b. einen Software-MPEG-2-Decoder für die Verwendung mit dem [DVD-Navigator](dvd-navigator-filter.md)schreiben, müssen Sie eine dieser Schnittstellen implementieren und außerdem die DVD-bezogenen Eigenschaften Sätze unterstützen, die der Navigator an den Decoder sendet. Pins können eine dieser Schnittstellen unterstützen, damit andere Pins oder Filter Ihre Eigenschaften festlegen oder abrufen können.

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die im DirectShow-DDK dokumentierte " **ikscontrol** "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

## <a name="members"></a>Member

Die " **ikspropertyset** "-Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. " **Ikspropertyset** " verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die " **ikspropertyset** "-Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Erhalten**](ikspropertyset-get.md)                       | Ruft eine Eigenschaft ab, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.<br/> |
| [**Querysupported**](ikspropertyset-querysupported.md) | Bestimmt, ob ein Objekt einen angegebenen Eigenschaften Satz unterstützt.<br/>           |
| [**Set**](ikspropertyset-set.md)                       | Legt eine Eigenschaft fest, die durch eine Eigenschaften Satz-GUID und eine eigen schafts-ID identifiziert wird.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen "KS. h" vor "ksproxy. h" einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 
