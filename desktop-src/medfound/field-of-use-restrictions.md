---
description: Nutzungseinschränkungen
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Nutzungseinschränkungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccfb5b7c0923bdea117371a3b6af2669bf903fb3af996f754be43d5665c1ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942670"
---
# <a name="field-of-use-restrictions"></a>Nutzungseinschränkungen

> [!Note]  
> Dieses Thema gilt für Windows 7 oder höher.

 

Eine *Verwendungseinschränkung ist eine* Bereitstellung, die die Verwendung einer Lizenz für eine bestimmte Technologie einschränkt.

Media Foundation bietet einen Mechanismus zum Erzwingen von Nutzungseinschränkungen für Media Foundation Transformationen (MFTs), insbesondere Codecs. Dieser Mechanismus erfordert, dass MFT seine eigene Verwendung durch Anwendungen blockiert, bis die Anwendung einen Handshake mit dem MFT ausgeführt hat. Media Foundation den Handshake nicht definiert– in der Regel würde dies einen kryptografischen Austausch beinhalten.

### <a name="registration-and-enumeration"></a>Registrierung und Enumeration

Wenn für ein MFT Nutzungseinschränkungen gelten, legen Sie das **Flag MFT \_ ENUM \_ FLAG \_ FIELDOFUSE** fest, wenn Sie MFT registrieren. Dieses Flag gilt für die folgenden MFT-Registrierungs-APIs:

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**BLOCKSLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

Standardmäßig werden MFTs, die mit diesem Flag registriert sind, aus den Enumerationsergebnissen ausgeschlossen. Rufen Sie [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) auf, und geben Sie im Flags-Parameter das **Flag MFT \_ ENUM \_ FLAG \_ FIELDOFUSE** an, um MFTs mit *Verwendungseinschränkungen aufzählen* zu können. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm, das mft und eine Anwendung zeigt, die Daten an die Registrierung sendet](images/mft-fou01.gif)

Die [**MFTEnum-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) schließt immer alle MFTs mit Nutzungseinschränkungen aus.

### <a name="unlocking-the-mft"></a>Entsperren des MFT

Führen Sie die folgenden Schritte aus, um MFT mit Nutzungseinschränkungen zu verwenden:

1.  Die Anwendung implementiert die [**BERFTF-Schnittstelle .B.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)
2.  Die METHODE 100000011100007 verwendet einen Zeiger auf die **IUnknown-Schnittstelle** von MFT. [](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock)
3.  In der [**Unlock-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) führt die Anwendung den erforderlichen Handshake mithilfe des vom MFT definierten Mechanismus aus. Dieser Schritt wird nicht von der Media Foundation DEFINIERT.
4.  Wenn die [**Unlock-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) erfolgreich ist, entsperrt sich MFT selbst.

Die Anwendung gibt den [**ZEIGER AUF DAS FELDOFUSE UNLOCK-Attribut**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) [(MFT \_ FIELDOFUSE \_ UNLOCK \_ Attribute)](mft-fieldofuse-unlock-attribute.md) an. Je nachdem, wie Ihre Anwendung den Decoder oder die Codierungspipeline erstellt, gibt es verschiedene Möglichkeiten, dieses Attribut zu festlegen:



| API                   | Entsperren des Verwendungsfelds                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quellleser         | Wenn Ihre Anwendung [](source-reader.md) den Quellleser zum Decodieren einer Mediendatei verwendet, legen Sie das [Attribut MFT \_ FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md) in den Konfigurationsparametern fest. Weitere Informationen [finden Sie unter Quellleseattribute.](source-reader-attributes.md)                                                                                                                                                                                                                                                                         |
| Sink Writer           | Wenn Ihre Anwendung den Senkenwriter zum Codieren einer Mediendatei verwendet, legen Sie das [Attribut MFT \_ FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md) in den Konfigurationsparametern fest. Weitere Informationen [finden Sie unter Sink Writer-Attribute.](sink-writer-attributes.md)                                                                                                                                                                                                                                                                                                    |
| Schnelle Transcodierung        | Wenn Ihre Anwendung das Feature "Fast Transcode" verwendet, um eine Codierungstopologie zu erstellen, legen Sie das [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md) fest, wenn Sie [**DIEDTRANSCODEProfile::SetContainerAttributes aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) Weitere Informationen zum Feature "Schnelle Transcodierung" finden Sie unter [Transcodierungs-API](transcode-api.md).                                                                                                                                                                      |
| Topologie              | Wenn Sie eine Topologie direkt erstellen, legen Sie das [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md) als Attribut für die Topologie fest. Weitere Informationen [finden Sie unter Topologieattribute.](topology-attributes.md)                                                                                                                                                                                                                                                                                                                                                  |
| MFT-Aktivierungsobjekt | Wenn Ihre Anwendung die zu verwendenden Decoder oder Encoder direkt aufzählt, legen Sie das [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md) für die VON der [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zurückgegebenen [**UNLOCKActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) fest. <br/> Legen Sie das -Attribut fest, bevor Sie ZUM ERSTELLEN des [**MFT-Objekts DIEACTIVate::ActivateObject-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) aufrufen. Das Aktivierungsobjekt ruft [**BEIM Erstellen des MFT-Objekts DEN Aufruf VON DURCHEFIELDOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) auf.<br/> |



 

Das folgende Diagramm zeigt die Beziehung zwischen MFT-Aktivierungsobjekten und [**der BENUTZEROBERFLÄCHEFieldOfUseMFTUnlock-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)

![Diagramm, das eine Anwendung, ein Aktivierungsobjekt und Mft mit Pfeilen zu einem FOU-Objekt zeigt, das über einen Pfeil zurück zu Mft verfügt](images/mft-fou02.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 




