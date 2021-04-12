---
title: /Protocol-Schalter
description: Der/Protocol-Schalter gibt an, welches Wire-Protokoll vom generierten Stub unterstützt wird.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /Protocol-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313025"
---
# <a name="protocol-switch"></a>/Protocol-Schalter

Der **/Protocol** -Schalter gibt an, welches Wire-Protokoll vom generierten Stub unterstützt wird.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>DCE * * * *


</dt> <dd>

Der generierte Stub unterstützt nur das DCE-Protokoll.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

Der generierte Stub unterstützt nur das Microsoft NDR64-Protokoll.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>Alle * * * *


</dt> <dd>

Der generierte Stub unterstützt alle verfügbaren Protokolle für eine bestimmte Umgebung.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

RPC marshallt und entmarshallt Daten gemäß einem Strict-Übertragungsprotokoll (auch Übertragungs Syntax genannt), das die Daten Übertragungs Darstellung definiert, wie z. b. die Reihenfolge, in der Datenmember gemarshallt werden, die Ausrichtung der Daten im Netzwerk, zusätzliche Informationen, die in den Daten enthalten sind. Microsoft RPC ist mit dem Protokoll von OSF-DCE (Netzwerkdaten Darstellung) kompatibel. In der 64-Bit-Version von Windows XP führt Microsoft ein experimentelles Protokoll NDR64 ein, das für die Übertragung von 64-Bit-Daten optimiert ist. NDR64 ist nicht abwärts kompatibel mit dem DCE-Protokoll.

Das **DCE** -Protokoll ist mit der NDR-Übertragungs Syntax von OSF DCE kompatibel. Dieses Protokoll ist für die Übertragung von 32-Bit-Daten optimiert.

Das **ndr64** -Protokoll wird zurzeit nur unterstützt, wenn es in Verbindung mit dem [**/Win64**](-win64.md) -Switch verwendet wird. Wenn ein ndr64 only-Client versucht, eine Verbindung mit einem nur DCE-Server herzustellen (oder umgekehrt), wird der Aufruf mit der \_ \_ nicht unterstützten Transaktionsdatei RPC S abgelehnt \_ \_ .

Mit der Option **all** wird ein Stub erstellt, von dem jedes verfügbare Protokoll verwendet werden kann. Bei 32-Bit-stubwerten ist das einzige derzeit verfügbare Protokoll DCE. Bei 64-Bit-stubwerten, die mit dem Schalter [**/Win64**](-win64.md) erstellt wurden, sind sowohl DCE als auch NDR64 verfügbar.

## <a name="examples"></a>Beispiele

**Mittel l/Protocol alle/Win64 filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




