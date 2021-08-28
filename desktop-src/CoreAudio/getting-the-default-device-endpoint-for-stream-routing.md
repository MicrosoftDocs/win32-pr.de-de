---
description: In Windows 7 implementieren high-level-Plattform-APIs, die Core Audio-APIs wie Media Foundation, DirectSound und Wave-APIs verwenden, das Streamroutingfeature, indem sie den Streamwechsel von einem vorhandenen Gerät zu einem neuen Standardaudioendpunkt verarbeiten.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Abrufen des Geräteendpunkts für das Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb45560bc8a27e4641e5d52c8fed0bee51c877dbec4d098bb5232830359f0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695390"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Abrufen des Geräteendpunkts für das Streamrouting

In Windows 7 implementieren high-level-Plattform-APIs, die Core Audio-APIs wie Media Foundation, DirectSound und Wave-APIs verwenden, das Streamroutingfeature, indem sie den Streamwechsel von einem vorhandenen Gerät zu einem neuen Standardaudioendpunkt verarbeiten. Medienanwendungen, die diese APIs verwenden (z. B. eine Anwendung, die ein **IDirectSound-** oder **IBaseFilter-Objekt** für ein [**IMMDevice-Objekt**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) aktiviert), verwenden das Streamroutingverhalten ohne Änderungen an der Quelle.

Die übergeordneten APIs implementieren das Streamrouting für den Geräteendpunkt, der über [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)abgerufen wird. Wenn eine Anwendung an das Standardgerät gestreamt wird, funktioniert das Streamroutingfeature wie definiert. Streams werden nicht auf das neue Gerät umgestellt, wenn es von einem anderen Mechanismus abgerufen wird, auch wenn es mit dem Standardgerät identisch ist.

Eine Medienanwendung, die Core Audio-APIs direkt verwendet (WASAPI-Client), kann eine benutzerdefinierte Streamroutingimplementation für jedes Rendering- oder Erfassungsgerät bereitstellen. Ein WASAPI-Client kann die von den übergeordneten APIs bereitgestellte Implemetation replizieren, indem er ihn auf Datenströme beschränkt, die auf Geräten geöffnet sind, die als Standardgerät festgelegt sind. Um einen Verweis auf den Endpunkt des Standardgeräts abzurufen, muss der Client [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufrufen. In diesem Aufruf muss der Client angeben, ob ein Zeiger auf das Renderingstandardgerät oder das Standardgerät für die Erfassung erforderlich ist, indem der *DataFlow-Parameter* angegeben wird. Der Client muss auch die entsprechende Rolle für den Endpunkt im **ERole-Attribut** angeben (**eConsole** oder **eCommunications**). Verwenden Sie **eMultimedia** nicht.

Wenn die Anwendung an ein anderes Gerät gestreamt wird, kann die Anwendung das Gerät abrufen, indem sie eine Endpunkt-ID-Zeichenfolge angibt (durch Aufrufen von [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Nachdem das Gerät identifiziert wurde, kann der WASAPI-Client die Implementierung für das Streamrouting bereitstellen, indem er die für das Gerät gesendeten Geräte- und Audiositzungsbenachrichtigungen verarbeitet. Weitere Informationen zu diesen Benachrichtigungen finden Sie unter [Relevante Benachrichtigungen für Streamrouting.](relevant-device-notifications-for-stream-routing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur MMDevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



