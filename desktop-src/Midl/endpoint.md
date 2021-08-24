---
title: Endpunktattribut
description: Das Attribut \endpoint\ gibt einen bekannten Port oder ports (Kommunikationsendpunkte) an, an denen Server der Schnittstelle auf Aufrufe lauschen.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- Endpunktattribut MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea4951a407f09c1407c6e897938460d780e0429e888210e7e1ade392b5e94af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383180"
---
# <a name="endpoint-attribute"></a>Endpunktattribut

Das **\[ \] Endpunktattribut** gibt einen bzw. mehrere bekannte Ports (Kommunikationsendpunkte) an, an denen Server der Schnittstelle auf Aufrufe lauschen.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokollsequenz* 
</dt> <dd>

Gibt eine Zeichenfolge an, die eine gültige Kombination aus einem RPC-Protokoll (z. B. "ncacn"), einem Transportprotokoll (z.B. "tcp") und einem Netzwerkprotokoll (z. B. "ip") darstellt. Eine Liste der gültigen Protokollsequenzen finden Sie unter [Protokollsequenzkonst constants](/windows/desktop/Rpc/protocol-sequence-constants).

</dd> <dt>

*endpoint-port* 
</dt> <dd>

Gibt eine Zeichenfolge an, die die Endpunktbezeichnung für die angegebene Protokollfamilie darstellt. Die Syntax der Portzeichenfolge ist für jede Protokollsequenz spezifisch.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \] Endpunktattribut** gibt eine Transportfamilie an, z. B. das tcp/IP-verbindungsorientierte Protokoll, ein netBIOS-verbindungsorientiertes Protokoll oder das verbindungsorientierte Named Pipe-Protokoll. Die Verwendung des **\[ \] Endpunktattributs** ist konsistent mit anderen Methoden zum Hinzufügen eines Endpunkts und stellt keine zusätzlichen oder speziellen Dienste für den Endpunkt bereit. Es stellt lediglich eine Verknüpfung zum Aufrufen der API bereit.

> [!Note]  
> Angeben eines Endpunkts in der . Die Definition der IDL-Schnittstelle schränkt den Zugriff auf die Schnittstelle auf den angegebenen Endpunkt nicht ein. Hinzufügen eines Endpunkts zum . Mit der IDL-Schnittstellendefinition kann die Schnittstelle über einen beliebigen Endpunkt in diesem Prozess aufgerufen werden, und der Endpunkt kann zum Aufrufen anderer Schnittstellen in diesem Prozess verwendet werden.

 

Der *Protokollsequenzwert bestimmt* die gültigen Werte für *den Endpunktport*. Der MIDL-Compiler überprüft nur die allgemeine Syntax für den *Endpunktporteintrag.* Portspezifikationsfehler werden von den Laufzeitbibliotheken gemeldet. Informationen zu den zulässigen Werten für jede Protokollsequenz finden Sie unter [Protokollsequenzkonst constants](/windows/desktop/Rpc/protocol-sequence-constants).

Die folgenden von DCE angegebenen Protokollsequenzen werden vom MIDL-Compiler, der mit Microsoft RPC bereitgestellt wird, nicht unterstützt: **ncacn \_ osi \_ dna** und **ncadg \_ dds**.

Stellen Sie sicher, dass Sie schräge Schrägstriche in Endpunkten richtig anführungszeichen anführungszeichen. Dieser Fehler tritt häufig auf, wenn der Endpunkt eine Named Pipe ist.

Die in der IDL-Datei angegebenen Endpunktinformationen werden von den RPC-Laufzeitfunktionen [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) und [**RpcServerUseAllProtseqsIf verwendet.**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)

## <a name="examples"></a>Beispiele

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 