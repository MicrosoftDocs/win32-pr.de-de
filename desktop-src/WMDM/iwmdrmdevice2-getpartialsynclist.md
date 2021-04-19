---
title: IWMDRMDevice2 getpartialsynclist-Methode
description: Die getpartialsynclist-Methode ruft eine partielle Synchronisierungs Liste ab.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Getpartialsynclist-Methode, Windows Media Device Manager
- Getpartialsynclist-Methode Windows Media Device Manager, IWMDRMDevice2-Schnittstelle
- IWMDRMDevice2 Interface Windows Media Device Manager, getpartialsynclist-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367776"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>IWMDRMDevice2:: getpartialsynclist-Methode

Die **getpartialsynclist** -Methode ruft eine partielle Synchronisierungs Liste ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cminzählthreshold* \[ in\]
</dt> <dd>

Schwellenwert für minimale Anzahl.

</dd> <dt>

*cminhoursthreshold* \[ in\]
</dt> <dd>

Schwellenwert für minimale Stunden.

</dd> <dt>

*dwstartingindex* \[ in\]
</dt> <dd>

Die Start Position für die Indizierung.

</dd> <dt>

*cItems* \[ in\]
</dt> <dd>

Anzahl der zu indizierenden Elemente.

</dd> <dt>

*ppbsynclist* \[ vorgenommen\]
</dt> <dd>

Abgerufene Lizenz Synchronisierungs Liste.

</dd> <dt>

*pcbsynclist* \[ vorgenommen\]
</dt> <dd>

Größe der Lizenz Synchronisierungs Liste in Bytes.

</dd> <dt>

*pdwnextstartingindex* \[ vorgenommen\]
</dt> <dd>

Nächste Anfangsposition für die Indizierung.

</dd> <dt>

*pcitemsprocgelassene* \[ vorgenommen\]
</dt> <dd>

Anzahl der Elemente, die verarbeitet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Alle Schnittstellen Methoden in Windows Media Device Manager können eine der folgenden Klassen von Fehlercodes zurückgeben:

-   Standard-COM-Fehlercodes
-   In HRESULT-Werte konvertierte Windows-Fehlercodes
-   Fehlercodes für Windows Media Device Manager

Eine umfassende Liste möglicher Fehlercodes finden Sie unter [Fehlercodes](error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmddrmsp. idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmdevice:: getsynclist**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**IWMDRMDevice2-Schnittstelle**](iwmdrmdevice2.md)
</dt> </dl>

 

 





