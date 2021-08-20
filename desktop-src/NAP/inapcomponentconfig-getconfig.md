---
title: INapComponentConfig-GetConfig-Methode (NapCommon.h)
description: Ruft die ShV-Komponentenkonfiguration (System Health Validator) ab.
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig-Methode NAP
- GetConfig-Methode NAP, INapComponentConfig-Schnittstelle
- INapComponentConfig-Schnittstelle NAP, GetConfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dc5495df10e3a5ff3907941644c5558aea35d29b52c8773fb56314c4a8620c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134498"
---
# <a name="inapcomponentconfiggetconfig-method"></a>INapComponentConfig::GetConfig-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **GetConfig-Methode** ruft die ShV-Komponentenkonfiguration (System Health Validator) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bCount* \[ out\]
</dt> <dd>

Die Größe des Datenkonfigurationsblobs in Bytes. 

</dd> <dt>

*Daten* \[ out\]
</dt> <dd>

Ein Zeiger auf die Adresse der Konfigurationsdaten der SHV-Komponente.

> [!Note]  
> Konfigurationsdaten, die mithilfe der **GetConfig-Methode** von einem x86-Computer exportiert werden, können mithilfe der [**SetConfig-Methode**](inapcomponentconfig-setconfig.md) auf einen x64-Computer importiert werden und umgekehrt. Daher müssen Konfigurationsdaten in einem architekturunabhängigen Format wie XML vorliegen. Die Verwendung von XML anstelle eines Bytestreams erleichtert die Verwendung von Konfigurationsdaten in verschiedenen Architekturen. Die in den Konfigurationsdaten verwendeten XML-Elemente werden vom Implementierer bestimmt.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Datenparameter muss vom Aufgerufenen (Komponenten implementor) mithilfe von **CoTaskMemAlloc** zugeordnet und vom Aufrufer mit **coTaskMemFree** freigegeben werden.

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

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





