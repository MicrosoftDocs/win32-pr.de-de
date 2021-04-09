---
title: Endpunkt Attribut
description: Das Attribut \ Endpoint \ gibt einen bekannten Port oder Ports (Kommunikations Endpunkte) an, auf denen Server der Schnittstelle auf Aufrufe lauschen.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- Endpunkt Attribut-Mittel l
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858175"
---
# <a name="endpoint-attribute"></a>Endpunkt Attribut

Das **\[ Endpunkt \]** Attribut gibt einen bekannten Port oder Ports (Kommunikations Endpunkte) an, auf denen Server der Schnittstelle auf Aufrufe lauschen.

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Protokoll Sequenz* 
</dt> <dd>

Gibt eine Zeichenfolge an, die eine gültige Kombination eines RPC-Protokolls (z. b. "ncacn"), eines Transport Protokolls (z. b. "TCP") und eines Netzwerk Protokolls (z. b. "IP") darstellt. Eine Liste der gültigen Protokoll Sequenzen finden Sie unter [Protokoll Sequenz Konstanten](/windows/desktop/Rpc/protocol-sequence-constants).

</dd> <dt>

*Endpunkt-Port* 
</dt> <dd>

Gibt eine Zeichenfolge an, die die Endpunkt Bezeichnung für die angegebene Protokollfamilie darstellt. Die Syntax der Port Zeichenfolge ist spezifisch für jede Protokoll Sequenz.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Endpunkt \]** Attribut gibt eine Transport Familie an, z. b. das Verbindungs orientierte TCP/IP-Protokoll, ein NetBIOS-Verbindungs orientiertes Protokoll oder das Verbindungs orientierte Named Pipe-Protokoll. Die Verwendung des **\[ Endpunkt \]** Attributs ist mit anderen Methoden zum Hinzufügen eines Endpunkts konsistent und bietet keine zusätzlichen oder speziellen Dienste für den Endpunkt. er bietet lediglich eine Verknüpfung zum Aufrufen der API.

> [!Note]  
> Angeben eines Endpunkts in. Die IDL-Schnittstellen Definition schränkt den Zugriff auf die-Schnittstelle nicht auf den angegebenen Endpunkt ein. Hinzufügen eines Endpunkts zu. Mithilfe der IDL-Schnittstellen Definition kann die Schnittstelle über einen beliebigen Endpunkt in diesem Prozess aufgerufen werden, und der Endpunkt kann verwendet werden, um andere Schnittstellen in diesem Prozess aufzurufen.

 

Der *Protokoll Sequenz* Wert bestimmt die gültigen Werte für den *Endpunkt-Port*. Der mittlerer l-Compiler prüft nur die allgemeine Syntax für den *Endpunkt-Port-* Eintrag. Port Spezifikations Fehler werden von den Laufzeitbibliotheken gemeldet. Informationen zu den zulässigen Werten für jede Protokoll Sequenz finden Sie unter den [Protokoll Sequenz Konstanten](/windows/desktop/Rpc/protocol-sequence-constants).

Die folgenden durch DCE angegebenen Protokoll Sequenzen werden von dem mit Microsoft RPC: **ncacn \_ OSI \_ DNA** und **ncadg \_ DDS** bereitgestellten Mittell-Compiler nicht unterstützt.

Stellen Sie sicher, dass Sie umgekehrte Schrägstriche in Endpunkten ordnungsgemäß angeben. Dieser Fehler tritt häufig auf, wenn der Endpunkt eine Named Pipe ist.

Die in der IDL-Datei angegebenen Endpunkt Informationen werden von den RPC-Lauf Zeitfunktionen [**rpcserveruseprotabqif**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) und [**rpcserveruseallprotsqsif**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)verwendet.

## <a name="examples"></a>Beispiele

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Rpcserveruseallprotabqsif**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[**Rpcserveruseprotabqif**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 