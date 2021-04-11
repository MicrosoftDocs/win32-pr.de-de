---
description: Erstellt die angegebene-Schnittstelle.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Iscardmanage:: up-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217330"
---
# <a name="iscardmanagecreateinterface-method"></a>Iscardmanage:: up-Methode

\[Die **Methode "** Methode" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Methode "** Methode" erstellt die angegebene Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguidinterface* \[ in\]
</dt> <dd>

Der GUID-Wert der zu erstellenden Schnittstelle.

</dd> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Der Name der Schnittstelle, die erstellt werden soll, wenn die GUID nicht verfügbar ist. Standard Werte sind "CryptoProvider".

</dd> <dt>

*puserdata* \[ in\]
</dt> <dd>

Zeiger auf benutzerspezifische Daten, die beim Erstellen einer Schnittstelle verwendet werden sollen.

</dd> <dt>

*ppinterface* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die zurückgegebene Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>                                                     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Einer der angegebenen Parameter ist ungültig.<br/>                                         |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Ein fehlerhafter Zeiger wurde entweder im *pguidinterface* -oder im *puserdata* -Parameter übergeben.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste aller Methoden, die von der [**iscardmanage**](iscardmanage.md) -Schnittstelle definiert werden, finden Sie unter **iscardmanage**.

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardmanage**](iscardmanage.md)
</dt> </dl>

 

 
