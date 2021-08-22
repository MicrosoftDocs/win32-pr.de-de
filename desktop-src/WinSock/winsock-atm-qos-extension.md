---
description: In diesem Abschnitt wird die protokollspezifische Quality of Service (QOS) für ATM beschrieben, die im Feld ProviderSpecific der QOS-Struktur enthalten ist.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Winsock ATM QoS-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422db2df8e4f845086120814f6cf4e6288dcc00c42693eac8da21c466448aaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612820"
---
# <a name="winsock-atm-qos-extension"></a>Winsock ATM QoS-Erweiterung

In diesem Abschnitt wird die protokollspezifische Quality of Service -Struktur [**(QOS)**](/windows/win32/api/winsock2/ns-winsock2-qos)für ATM beschrieben, die im [Feld ProviderSpecific](/previous-versions/aa374467(v=vs.80)) der **QOS-Struktur enthalten** ist. Beachten Sie, dass die Verwendung dieser ATM-spezifischen **QOS-Struktur** von Windows Sockets 2-Clients optional ist und der ATM-Dienstanbieter erforderlich ist, um die generische [**FLOWSPEC-Struktur**](/windows/win32/api/qos/ns-qos-flowspec) den entsprechenden Q.2931-Informationselementen zuordnen zu können. Wenn jedoch sowohl die generische **FLOWSPEC-Struktur** als auch die ATM-spezifische **QOS-Struktur** angegeben werden, sollte der in der ATM-spezifischen **QOS-Struktur** angegebene Wert Vorrang haben, falls Konflikte entstehen. Weitere Windows QoS-Bestimmungen und **flowsPEC-Struktur** finden Sie unter Sockets 2 API Specification Section 2.7 (Sockets 2-API-Spezifikation, Abschnitt 2.7).

Die protokollspezifische [**QOS-Struktur**](/windows/win32/api/winsock2/ns-winsock2-qos) für ATM ist eine Verkettung von Q.2931-Informationselementstrukturen (IE), die im folgenden Text definiert sind. Wenn eine Anwendung eine IE ausgelassen hat, die UNI 3.x vorträgt, sollte der Dienstanbieter einen angemessenen Standardwert einfügen und die Informationen in der [**FLOWSPEC-Struktur**](/windows/win32/api/qos/ns-qos-flowspec) ggf. berücksichtigen.

Die Behandlung von wiederholten IEs hängt von der Internet-E/A selbst ab. Wenn ein Internet-E/A wiederholt wird und es sich um einen IE handelt, der entsprechend der ATM Forum UNI-Spezifikation wiederholt werden darf, muss der Anbieter ihn ordnungsgemäß behandeln. In diesem Fall bestimmt die Reihenfolge in der Liste die Einstellungs reihenfolge, bei der Elemente, die früher in der Liste angezeigt werden, bevorzugt werden. Wenn eine Internetzugriffs-E/A wiederholt wird und dies pro ATM Forum UNI-Spezifikation nicht zulässig ist, kann der Anbieter entweder die Anforderung vom Client (die bevorzugte Option) fehlschlagen oder die letzte gefundene IE dieses Typs verwenden.

Jede einzelne IE-Struktur wird wie folgt formatiert und durch das **IEType-Feld** identifiziert:

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Die rechtlichen Werte für das **Feld IEType** sind wie die folgenden definiert:

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

Das **IE-Feld** wird durch eine bestimmte IE-Struktur überlagert, und das **IELength-Feld** ist die Gesamtlänge in Bytes der IE-Struktur, einschließlich der **Felder IEType** und **IELength.** Die Semantik und die rechtlichen Werte für jedes Element dieser IE-Strukturen entsprechen der ATM UNI 3.x-Spezifikation. SAP FIELD ABSENT kann für die Elemente verwendet werden, die für eine bestimmte IE-Struktur nach \_ \_ ATM UNI 3.x-Spezifikation optional sind.

 

 
