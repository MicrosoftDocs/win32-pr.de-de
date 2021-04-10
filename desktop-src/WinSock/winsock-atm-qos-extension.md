---
description: In diesem Abschnitt wird die Protokoll spezifische Quality of Service Struktur (QoS) für ATM beschrieben, die im Feld ProviderSpecific der QoS-Struktur enthalten ist.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Winsock ATM-QoS-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129105"
---
# <a name="winsock-atm-qos-extension"></a>Winsock ATM-QoS-Erweiterung

In diesem Abschnitt wird die Protokoll spezifische Quality of Service Struktur ([**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)) für ATM beschrieben, die im Feld [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) der **QoS** -Struktur enthalten ist. Beachten Sie, dass die Verwendung dieser ATM-spezifischen **QoS** -Struktur von Windows Sockets 2-Clients optional ist, und der ATM-Dienstanbieter ist erforderlich, um die generische [**Flowspec**](/windows/win32/api/qos/ns-qos-flowspec) -Struktur den entsprechenden Q. 2931-Informations Elementen zuzuordnen. Wenn jedoch sowohl die generische **Flowspec** -Struktur als auch die ATM-spezifische **QoS** -Struktur angegeben werden, sollte der in der ATM-spezifischen **QoS** -Struktur angegebene Wert Vorrang haben, wenn Konflikte auftreten. Weitere Informationen zu QoS-und **Flowspec** -Strukturen finden Sie im Abschnitt 2,7 der Windows Sockets 2-API-Spezifikation.

Die Protokoll spezifische [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) -Struktur für ATM ist eine Verkettung von Q. 2931 Information Element-Strukturen (IE), die im folgenden Text definiert werden. Wenn eine Anwendung einen Internetinformationsdienst (IE) auslässt, den die Uni 3. x nicht benötigt, sollte der Dienstanbieter einen angemessenen Standardwert einfügen, wobei die Informationen in der [**Flowspec**](/windows/win32/api/qos/ns-qos-flowspec) -Struktur ggf. berücksichtigt werden.

Die Behandlung von wiederholten Wiederholungen hängt von der IE selbst ab. Wenn ein Internet Explorer wiederholt wird und es sich um einen Wert handelt, der gemäß der Uni-Spezifikation des ATM-Forums wiederholt werden darf, muss der Anbieter ihn ordnungsgemäß behandeln. In diesem Fall bestimmt Order in der Liste die bevorzugte Reihenfolge, wobei Elemente, die an früherer Stelle in der Liste angezeigt werden, besser bevorzugt werden. Wenn ein Internet Explorer wiederholt wird und dies nicht pro ATM-Forums-UNI-Spezifikation zulässig ist, kann der Anbieter entweder die Anforderung vom Client (die bevorzugte Option) nicht ausführen oder den letzten IE dieses Typs verwenden.

Jede einzelne IE-Struktur wird wie folgt formatiert und durch das **ietype** -Feld identifiziert:

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Zulässige Werte für das **ietype** -Feld werden wie folgt definiert:

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

Das Feld " **IE** " wird durch eine bestimmte IE-Struktur überlagert, und das Feld " **ielength** " ist die Gesamtlänge in Byte der IE-Struktur, einschließlich der **ietype** -und **ielength** -Felder. Die Semantik und die gültigen Werte für jedes Element dieser IE-Strukturen sind gemäß der ATM-Uni 3. x-Spezifikation. Ein nicht vorhandenes SAP- \_ Feld \_ kann für die Elemente verwendet werden, die für eine bestimmte IE-Struktur optional sind, und zwar gemäß der Angabe von ATM Uni 3. x

 

 
