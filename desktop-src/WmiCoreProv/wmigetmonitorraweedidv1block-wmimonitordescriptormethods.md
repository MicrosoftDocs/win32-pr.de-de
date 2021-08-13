---
description: Ruft die Rohdaten für eine angegebene E-EDID-Struktur (Video Electronics Standard Association) Enhanced Extended Display Identification Data (VESA) ab, die optimale Einstellungen für die Konfiguration eines Monitors definiert.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: WmiGetMonitorRawEEdidV1Block-Methode der WmiMonitorDescriptorMethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: dacd0c44a6c0fa8270a65155583f8041616f98674d0798db8b13a72d13751653
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558085"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>WmiGetMonitorRawEEdidV1Block-Methode der WmiMonitorDescriptorMethods-Klasse

Die **WmiGetMonitorRawEEdidV1Block-Methode** ruft die Rohdaten für eine angegebene VeSA-Struktur (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID) ab, die optimale Einstellungen für die Konfiguration eines Monitors definiert.

## <a name="syntax"></a>Syntax


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BlockId* \[ In\]
</dt> <dd>

Die Datenblockidentität.

</dd> <dt>

*BlockType* \[ out\]
</dt> <dd>

Typ des Datenblocks. In der folgenden Tabelle sind mögliche Rückgabewerte aufgeführt.



| Wert                                                                                 | Bedeutung                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Uninitialized<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | EDID-Basisblock<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | EDID-Blockzuordnung<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Andere<br/>           |



 

</dd> <dt>

*BlockContent* \[ out\]
</dt> <dd>

Ein 128-Byte-Array, das den rohen Blockinhalt enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt null (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel werden die EDID-Blöcke einer beliebigen Anzeige als unformatierte 128-Bit-Arrays abgerufen.


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

