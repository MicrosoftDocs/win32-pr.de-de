---
title: Konstanten auf Authentifizierungs Ebene (rpcdce. h)
description: Diese Werte geben eine Authentifizierungs Ebene an, die angibt, welche Menge an Authentifizierung zur Verfügung steht, um die Integrität der Daten zu schützen. Jede Ebene enthält den Schutz, der von den vorherigen Ebenen bereitgestellt wird.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519063"
---
# <a name="authentication-level-constants"></a>Konstanten auf Authentifizierungs Ebene

Diese Werte geben eine Authentifizierungs Ebene an, die angibt, welche Menge an Authentifizierung zur Verfügung steht, um die Integrität der Daten zu schützen. Jede Ebene enthält den Schutz, der von den vorherigen Ebenen bereitgestellt wird.



| Konstante/Wert                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ \_ \_ \_ Standardwert für C-authn-Ebene**</dt> <dt>0</dt> </dl>                    | Weist DCOM an, die Authentifizierungs Ebene mithilfe des normalen sicherheitspausierungsalgorithmus auszuwählen. Weitere Informationen finden Sie unter [sicherheitspauschere Aushandlung](security-blanket-negotiation.md). <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ authn \_ Level \_ None**</dt> <dt>1</dt> </dl>                             | Führt keine Authentifizierung durch.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ authn \_ Level \_ Connect**</dt> <dt>2</dt> </dl>                    | Authentifiziert die Anmelde Informationen des Clients nur, wenn der Client eine Beziehung mit dem Server herstellt. Datagramm-Transporte verwenden \_ stattdessen immer RPC authn \_ Level \_ Pkt. <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ C \_ authn \_ Level \_**</dt> -Befehl <dt>3</dt> </dl>                             | Authentifiziert sich nur zu Beginn jedes Remote Prozedur Aufrufes, wenn der Server die Anforderung empfängt. Datagramm-Transporte \_ verwenden \_ stattdessen RPC C authn \_ Level \_ Pkt.<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ authn \_ Level \_ Pkt**</dt> <dt>4</dt> </dl>                                | Authentifiziert, dass alle empfangenen Daten vom erwarteten Client stammen.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ \_ \_ \_ Pkt- \_ Integrität der C-authn-Ebene**</dt> <dt>5</dt> </dl> | Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy**</dt> <dt>6</dt> </dl>       | Authentifiziert alle vorherigen Ebenen und verschlüsselt den Argument Wert jedes Remote Prozedur Aufrufes.<br/>                                                                                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





