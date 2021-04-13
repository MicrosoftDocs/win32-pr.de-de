---
title: Inapcomponentconfig GetConfig-Methode (napcommon. h)
description: Ruft die Konfiguration der System Integritätsprüfung (SHV) ab.
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig-Methode NAP
- GetConfig-Methode NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, GetConfig-Methode
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
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478444"
---
# <a name="inapcomponentconfiggetconfig-method"></a>Inapcomponentconfig:: GetConfig-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **GetConfig** -Methode ruft die Konfiguration der Systemintegritätsprüfungs-Komponente (SHV) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BCOUNT* \[ vorgenommen\]
</dt> <dd>

Die Größe des *Daten* konfigurationsblobs in Byte.

</dd> <dt>

*Daten* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Adresse der Konfigurationsdaten der SHV-Komponente.

> [!Note]  
> Konfigurationsdaten, die mithilfe der **GetConfig** -Methode von einem x86-Computer exportiert werden, können mithilfe der [**setconfig**](inapcomponentconfig-setconfig.md) -Methode auf einen x64-Computer importiert werden und umgekehrt. Daher müssen Konfigurationsdaten in einem Architektur agnostischen Format wie XML vorliegen. Durch die Verwendung von XML anstelle eines Bytestreams wird die Verwendung von Konfigurationsdaten auf verschiedenen Architekturen vereinfacht. Die XML-Elemente, die in den Konfigurationsdaten verwendet werden, werden durch den Implementierer bestimmt.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Data-Parameter muss vom aufgerufenen (komponentenimplementierer) mithilfe von **cotaskmemzuzugeordneten** zugewiesen und durch den Aufrufer mithilfe von " **CoTaskMemFree**" freigegeben werden.

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

[**Inapcomponentconfig:: setconfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





