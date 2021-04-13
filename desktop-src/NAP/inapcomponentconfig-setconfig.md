---
title: Inapcomponentconfig-setconfig-Methode (napcommon. h)
description: Legt die Konfiguration der Systemintegritätsprüfungs-Komponente (SHV) fest.
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Setconfig-Methode NAP
- Setconfig-Methode NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, setconfig-Methode
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
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519284"
---
# <a name="inapcomponentconfigsetconfig-method"></a>Inapcomponentconfig:: setconfig-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **setconfig** -Methode legt die Konfiguration der Systemintegritätsprüfungs-Komponente (SHV) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BCOUNT* \[ in\]
</dt> <dd>

Die Größe des *Daten* konfigurationsblobs in Byte.

</dd> <dt>

*Daten* \[ in\]
</dt> <dd>

Ein Zeiger auf die Konfigurationsdaten der SHV-Komponente.

> [!Note]  
> Konfigurationsdaten, die mithilfe der [**GetConfig**](inapcomponentconfig-getconfig.md) -Methode von einem x86-Computer exportiert werden, können mithilfe der **setconfig** -Methode auf einen x64-Computer importiert werden und umgekehrt. Daher müssen Konfigurationsdaten in einem Architektur agnostischen Format wie XML vorliegen. Durch die Verwendung von XML anstelle eines Bytestreams wird die Verwendung von Konfigurationsdaten auf verschiedenen Architekturen vereinfacht. Die XML-Elemente, die in den Konfigurationsdaten verwendet werden, werden durch den Implementierer bestimmt.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Informationen zur Versionsverwaltung von Komponenten sollten im datenkonfigurationsblob enthalten sein.  Die Versionsinformationen können verwendet werden, wenn von einer SHV-Version zu einer anderen migriert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapcomponentconfig**](inapcomponentconfig.md)
</dt> <dt>

[**Inapconponentconfig:: GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





