---
title: INapComponentConfig SetConfig-Methode (NapCommon.h)
description: Legt die Konfiguration der SHV-Komponentenkonfiguration (System Health Validator) fest.
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- SetConfig-Methode NAP
- SetConfig-Methode NAP, INapComponentConfig-Schnittstelle
- INapComponentConfig-Schnittstelle NAP, SetConfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3ecf455c591985a5e8778e49495351bd1b4aba83e9d29fe2b25d7d406a507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940198"
---
# <a name="inapcomponentconfigsetconfig-method"></a>INapComponentConfig::SetConfig-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **SetConfig-Methode** legt die Konfiguration der SHV-Komponenten (System Health Validator) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bCount* \[ In\]
</dt> <dd>

Die Größe des Datenkonfigurationsblobs in Bytes. 

</dd> <dt>

*data* \[ In\]
</dt> <dd>

Ein Zeiger auf die Konfigurationsdaten der SHV-Komponente.

> [!Note]  
> Konfigurationsdaten, die mithilfe der [**GetConfig-Methode**](inapcomponentconfig-getconfig.md) von einem x86-Computer exportiert werden, können mithilfe der **SetConfig-Methode** auf einen x64-Computer importiert werden und umgekehrt. Aus diesem Grund müssen Konfigurationsdaten in einem architekturunabhängigen Format vorliegen, z. B. XML. Die Verwendung von XML anstelle eines Bytestreams erleichtert die Verwendung von Konfigurationsdaten in verschiedenen Architekturen. Die in den Konfigurationsdaten verwendeten XML-Elemente werden vom Implementer bestimmt.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Komponentenversionsinformationen sollten im  Datenkonfigurationsblob enthalten sein. Die Versionsinformationen können bei der Migration von einer SHV-Version zu einer anderen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapConponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





