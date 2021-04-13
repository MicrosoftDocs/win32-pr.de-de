---
description: Einschränkungen bei der Verwendung des Felds
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Einschränkungen bei der Verwendung des Felds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16f57de7642fa789a08c886a32bf906faffb72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342469"
---
# <a name="field-of-use-restrictions"></a>Einschränkungen bei der Verwendung des Felds

> [!Note]  
> Dieses Thema gilt für Windows 7 oder höher.

 

Eine *Einschränkungs Einschränkung ist eine bereit* Stellung, die einschränkt, wie eine Lizenz für eine bestimmte Technologie verwendet werden kann.

Media Foundation bietet einen Mechanismus zum Erzwingen von Feld-in-use-Einschränkungen für Media Foundation Transformationen (MFTs), insbesondere bei Codecs. Dieser Mechanismus erfordert, dass der MFT seine eigene Verwendung durch Anwendungen blockiert, bis die Anwendung einen Handshake mit dem MFT ausgeführt hat. Media Foundation definiert nicht den Handshake – in der Regel würde es sich um eine Art kryptografieaustausch handeln.

### <a name="registration-and-enumeration"></a>Registrierung und Enumeration

Wenn eine MFT Einschränkungen für das Feld aufweist, legen Sie beim Registrieren des MFT das Flag " **\_ \_ \_ fieldofuse" für das MFT-Enum-Flag** fest. Dieses Flag gilt für die folgenden MFT-Registrierungs-APIs:

-   [**MF-tregiester**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MF-gisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MF tregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**Imflocalmf tregistration:: registermfts**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

Standardmäßig werden mit diesem Flag registrierte MFTs von enumerationsergebnissen ausgeschlossen. Um MFTs mit Einschränkungen für das Feld zu auflisten, nennen Sie [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , und geben Sie im *Flags* -Parameter das Flag **\_ \_ \_ fidofuse für das MFT-Enum-Flag** an. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm, das anzeigt, wie MFT und eine Anwendung Daten an die Registrierung senden](images/mft-fou01.gif)

Die [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion schließt immer alle MFTs aus, die Einschränkungen für das Feld verwenden.

### <a name="unlocking-the-mft"></a>Entsperren des MFT

Führen Sie die folgenden Schritte aus, um ein MFT mit Einschränkungen für das Feld zu verwenden:

1.  Die Anwendung implementiert die [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Schnittstelle.
2.  Die [**imffieldofusemftunlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) -Methode nimmt einen Zeiger auf die **IUnknown** -Schnittstelle der MFT auf.
3.  In der [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) -Methode führt die Anwendung den erforderlichen Handshake aus, wobei der von der MFT definierte Mechanismus verwendet wird. Dieser Schritt wird nicht durch Media Foundation-API definiert.
4.  Wenn die [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) -Methode erfolgreich ist, entsperrt sich die MFT selbst.

Die Anwendung gibt den [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger durch Festlegen des [MFT \_ fieldofuse \_ Unlock \_ Attribute](mft-fieldofuse-unlock-attribute.md) -Attributs an. Es gibt verschiedene Möglichkeiten, dieses Attribut festzulegen, je nachdem, wie die Anwendung den Decoder oder die Codierungs Pipeline erstellt:



| API                   | Entsperren des verwendeten Felds                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quell Leser         | Wenn Ihre Anwendung den [Quell Leser](source-reader.md) verwendet, um eine Mediendatei zu decodieren, legen Sie das Attribut Attribut [ \_ \_ Unlock \_ Attribut](mft-fieldofuse-unlock-attribute.md) in den Konfigurationsparametern fest. Siehe [Attribute des Quell Readers](source-reader-attributes.md).                                                                                                                                                                                                                                                                         |
| Senke-Writer           | Wenn Ihre Anwendung den senkenwriter verwendet, um eine Mediendatei zu codieren, legen Sie das Attribut Attribut [ \_ \_ Unlock \_ Attribut](mft-fieldofuse-unlock-attribute.md) in den Konfigurationsparametern fest. Siehe [senkenschreibattribute](sink-writer-attributes.md).                                                                                                                                                                                                                                                                                                    |
| Schnelles transcode        | Wenn Ihre Anwendung die Funktion "schnelles transcode" verwendet, um eine Codierungs Topologie zu erstellen, legen Sie das Attribut "Unlock" in [MFT \_ fieldofuse \_ \_](mft-fieldofuse-unlock-attribute.md) fest, wenn Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)aufrufen. Weitere Informationen zur Funktion "schnelles transcode" finden Sie unter [transcode-API](transcode-api.md).                                                                                                                                                                      |
| Topologie              | Wenn Sie eine Topologie direkt erstellen, legen Sie das Attribut "Unlock" von [MFT \_ fieldofuse \_ \_ ](mft-fieldofuse-unlock-attribute.md) als Attribut in der Topologie fest. Siehe [topologieattribute](topology-attributes.md).                                                                                                                                                                                                                                                                                                                                                  |
| MFT-Aktivierungs Objekt | Wenn Ihre Anwendung die Decoder oder Encoder direkt auflistet, die Sie verwenden werden, legen Sie das [Attribut "Unlock" von MFT \_ \_ \_ fieldofuse](mft-fieldofuse-unlock-attribute.md) auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, die von der Funktion " [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) " zurückgegeben werden. <br/> Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) zum Erstellen des MFT fest. Das Aktivierungs Objekt ruft [**imffieldofusemftunlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) auf, wenn die MFT erstellt wird.<br/> |



 

Das folgende Diagramm zeigt die Beziehung zwischen den MFT-Aktivierungs Objekten und der [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Schnittstelle.

![das Diagramm zeigt eine Anwendung, ein Aktivierungs Objekt und eine MFT mit Pfeilen zu einem Foundation-Objekt, das einen Pfeil zurück zu MFT hat.](images/mft-fou02.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 




