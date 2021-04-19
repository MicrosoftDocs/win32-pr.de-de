---
description: Ruft die unformatierten Daten für eine angegebene (durch VESA) erweiterte, erweiterte Display Identification Data (E-EDID)-Struktur (Video Electronics Standard Association) ab, die die optimalen Einstellungen für die Konfiguration eines Monitors definiert.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: WmiGetMonitorRawEEdidV1Block-Methode der wmimonitordescriptormethods-Klasse
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
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364158"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>WmiGetMonitorRawEEdidV1Block-Methode der wmimonitordescriptormethods-Klasse

Die **WmiGetMonitorRawEEdidV1Block** -Methode ruft die unformatierten Daten für eine angegebene (VESA) erweiterte, erweiterte Anzeige Identifikationsdaten (etedid)-Struktur (Video Electronics Standard Association) ab, die die optimalen Einstellungen für die Konfiguration eines Monitors definiert.

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

*Blockid* \[ in\]
</dt> <dd>

Die Datenblock Identität.

</dd> <dt>

*BlockType* \[ vorgenommen\]
</dt> <dd>

Der Typ des Datenblocks. In der folgenden Tabelle sind mögliche Rückgabewerte aufgeführt.



| Wert                                                                                 | Bedeutung                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Uninitialized<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | EDID-Basisblock<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | EDID-Block Zuordnung<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Sonstiges<br/>           |



 

</dd> <dt>

*Blockcontent* \[ vorgenommen\]
</dt> <dd>

Ein 128-Byte-Array, das den Rohdaten Block Inhalt enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL (0) zurück, um den Erfolg anzugeben. Jede andere Zahl gibt einen Fehler an. Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel werden die EDID-Blöcke jeder Anzeige als RAW-128-Bit-Arrays abgerufen.


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
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wmimonitordescriptormethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

