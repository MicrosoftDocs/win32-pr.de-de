---
description: In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs wie Media Foundation-, DirectSound-und Wave-APIs verwenden, das streamrouting-Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Der Geräte Endpunkt für das streamrouting wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861207"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>Der Geräte Endpunkt für das streamrouting wird erhalten.

In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs wie Media Foundation-, DirectSound-und Wave-APIs verwenden, das streamrouting-Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten. Medienanwendungen, die diese APIs verwenden (z. b. eine Anwendung, die ein **idirectsound** -oder **ibasefilter** -Objekt auf einem [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Objekt aktiviert), verwenden das Datenstrom-Routing Verhalten ohne Änderungen an der Quelle.

Die High-Level-APIs implementieren das Datenstrom Routing für den Geräte Endpunkt, der über [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)abgerufen wird. Wenn eine Anwendung auf das Standardgerät gestreamt wird, wird die streamweiterleitungs Funktion wie definiert angewendet. Streams werden nicht auf das neue Gerät umgestellt, wenn Sie von einem anderen Mechanismus abgerufen werden, auch wenn Sie mit dem Standardgerät identisch sind.

Eine Medien Anwendung, die Core-audioapis direkt (WASAPI-Client) verwendet, kann eine benutzerdefinierte streamweiterleitungs-Implementierung für jedes Rendering oder jedes Erfassungsgerät bereitstellen. Ein WASAPI-Client kann die von den APIs auf hoher Ebene bereitgestellte Implementierung replizieren, indem er auf Datenströme beschränkt wird, die auf Geräten geöffnet sind, die als Standardgerät festgelegt sind. Zum Abrufen eines Verweises auf den Endpunkt des Standard Geräts muss der Client " [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)" aufrufen. In diesem-Befehl muss der Client angeben, ob ein Zeiger auf das renderingstandardgerät oder das Erfassungs Standardgerät durch Angabe des *DataFlow* -Parameters erforderlich ist. Der Client muss auch die entsprechende Rolle für den Endpunkt im **erole** -Attribut angeben (**econsole** oder **eCommunications**). Verwenden Sie **emultimedia** nicht.

Wenn die Anwendung zu einem beliebigen anderen Gerät streamt, kann die Anwendung das Gerät abrufen, indem eine Endpunkt-ID-Zeichenfolge angegeben wird (durch den Aufruf von [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).

Nachdem das Gerät identifiziert wurde, kann der WASAPI-Client die Implementierung für das streamrouting bereitstellen, indem er die Geräte-und audiositzungsbenachrichtigungen verarbeitet, die für das Gerät gesendet werden. Weitere Informationen zu diesen Benachrichtigungen finden Sie unter [relevante Benachrichtigungen für das Datenstrom Routing](relevant-device-notifications-for-stream-routing.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über die mmdevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



